## Probando Numpy y Pandas

A continuación, se le brinda código en hojas de trucos disponibles en las herramientas Pandas y Numpy, las cuales debe probar cada código y brindar resultados por secciones, donde cada sección debe ir separada por una descripción en Markdown.

#### a. ¿Campo de aplicación de las librerías Pandas y Numpy?

NumPy es un paquete de Python que significa “Numerical Python”, es la librería principal para la informática científica, proporciona potentes estructuras de datos, implementando matrices y matrices multidimensionales. Estas estructuras de datos garantizan cálculos eficientes con matrices.

#### b. Utilizando la hoja de trucos de Numpy, pruebe cada uno de los códigos y muestre los resultados de cada sección.

### Creando Arrays


```python
import numpy as np

a = np.array([1,2,3])
b = np.array([(1.5,2,3), (4,5,6)], dtype = float)
c = np.array([[(1.5,2,3), (4,5,6)], [(3,2,1), (4,5,6)]], dtype = float)

```

#### Marcadores de posición iniciales


```python
np.zeros((3,4))               
np.ones((2,3,4),dtype=np.int16)
d = np.arange(10,25,5)
np.linspace(0,2,9)
e = np.full((2,2),7) 
f = np.eye(2)
np.random.random((2,2))
np.empty((3,2))
```




    array([[1.39069238e-309, 1.39069238e-309],
           [1.39069238e-309, 1.39069238e-309],
           [1.39069238e-309, 1.39069238e-309]])



### Guardar y cargar en disco


```python
np.save('my_array', a)
np.savez('array.npz', a, b)
np.load('my_array.npy')

```




    array([1, 2, 3])



### Guardar y cargar archivos de texto


```python
np.loadtxt("myfile.txt")
np.genfromtxt("my_file.csv", delimiter=',')
np.savetxt("myarray.txt", a, delimiter=" ")

```


    ---------------------------------------------------------------------------

    OSError                                   Traceback (most recent call last)

    <ipython-input-12-9fdd7007bdd7> in <module>
    ----> 1 np.loadtxt("myfile.txt")
          2 np.genfromtxt("my_file.csv", delimiter=',')
          3 np.savetxt("myarray.txt", a, delimiter=" ")
    

    F:\Instalacion\Anaconda\archivos\lib\site-packages\numpy\lib\npyio.py in loadtxt(fname, dtype, comments, delimiter, converters, skiprows, usecols, unpack, ndmin, encoding, max_rows)
        959             fname = os_fspath(fname)
        960         if _is_string_like(fname):
    --> 961             fh = np.lib._datasource.open(fname, 'rt', encoding=encoding)
        962             fencoding = getattr(fh, 'encoding', 'latin1')
        963             fh = iter(fh)
    

    F:\Instalacion\Anaconda\archivos\lib\site-packages\numpy\lib\_datasource.py in open(path, mode, destpath, encoding, newline)
        193 
        194     ds = DataSource(destpath)
    --> 195     return ds.open(path, mode, encoding=encoding, newline=newline)
        196 
        197 
    

    F:\Instalacion\Anaconda\archivos\lib\site-packages\numpy\lib\_datasource.py in open(self, path, mode, encoding, newline)
        533                                       encoding=encoding, newline=newline)
        534         else:
    --> 535             raise IOError("%s not found." % path)
        536 
        537 
    

    OSError: myfile.txt not found.


### Tipos de datos


```python
np.int64  
np.float32
np.complex
np.bool
np.object
np.string_
np.unicode_
```




    numpy.str_



### Inspección de su matriz


```python
a.shape  
len(a)
b.ndim
e.size
b.dtype   
b.dtype.name       
b.astype(int)
```




    array([[1, 2, 3],
           [4, 5, 6]])



### Pidiendo ayuda


```python
import numpy
np.info(np.ndarray.dtype)

```

    Data-type of the array's elements.
    
    Parameters
    ----------
    None
    
    Returns
    -------
    d : numpy dtype object
    
    See Also
    --------
    numpy.dtype
    
    Examples
    --------
    >>> x
    array([[0, 1],
           [2, 3]])
    >>> x.dtype
    dtype('int32')
    >>> type(x.dtype)
    <type 'numpy.dtype'>
    



### Arrays matematicos y Operaciones Aritmeticas


```python
 g = a - b ##sustraccion
([[-0.5, 0. , 0. ],
 [-3. , -3. , -3. ]])

np.subtract(a,b) 

b + a ##Adicion de arrays
([[ 2.5, 4. , 6. ],
[ 5. , 7. , 9. ]])
np.add(b,a) 

a / b ##Division
([[ 0.66666667, 1. , 1. ],
[ 0.25 , 0.4 , 0.5 ]])
np.divide(a,b)

a * b ##Multiplication
([[ 1.5, 4. , 9. ],
[ 4. , 10. , 18. ]])
np.multiply(a,b)

np.exp(b) ##Exponenciacion

np.sqrt(b) ## raiz cuadrada

np.sin(a) ##imprimir senos de una matriz

np.cos(b) ##coseno de elementos

np.log(a) ##logaritmo natural por elementos
    
e.dot(f) ##Dot product
([[ 7., 7.],
[ 7., 7.]])



```




    [[7.0, 7.0], [7.0, 7.0]]



### Comparación


```python
a == b 

```




    array([[False,  True,  True],
           [False, False, False]])




```python
a < 2 
```




    array([ True, False, False])




```python
 np.array_equal(a, b) 

```




    False



### Funciones agregadas


```python
a.sum()
```




    6




```python
a.min() ### Valor mínimo de arreglo
```




    1




```python
b.max(axis=0) ### Valor máximo de una fila de matriz
```




    array([4., 5., 6.])




```python
a.mean() 
```




    2.0




```python
np.median(b)
```




    3.5




```python
np.corrcoef(a) ### Coeficiente de correlación
```




    1.0




```python
np.std(b) ### desviacion standard
```




    1.5920810978785667




```python
b.cumsum(axis=1) ### Suma acumulativa de los elementos
```




    array([[ 1.5,  3.5,  6.5],
           [ 4. ,  9. , 15. ]])



### Copiar Arrays


```python
h = a.view()
```


```python
np.copy(a)
```




    array([1, 2, 3])




```python
h = a.copy()
```

### Ordenación de Arrays


```python
a.sort()
```


```python
c.sort(axis=0)
```

### Subconjunto, rebanado, indexación

#### Subconjunto


```python
a[2] ### Seleccione el elemento en el segundo índice
```




    3




```python
b[1,2] ### Seleccione el elemento en la fila 1, columna 2 (equivalente a b [1] [2])
```




    6.0



#### Rebanar


```python
a[0:2] ### Seleccionar elementos en el índice 0 y 1
```




    array([1, 2])




```python
b[0:2,1] ### Seleccionar elementos en las filas 0 y 1 en la columna 1
```




    array([2., 5.])




```python
b[:1] ### Seleccionar todos los elementos de la fila 0 (equivalente a b [0: 1,:])
```




    array([[1.5, 2. , 3. ]])




```python
c[1,...] ### La misma que [1,:,:]
```




    array([[3., 2., 3.],
           [4., 5., 6.]])




```python
a[ : :-1] ### Matriz invertida a
```




    array([3, 2, 1])



#### Indexación booleana


```python
a[a<2] ### Seleccione elementos de menos de 2
```




    array([1])



#### Indexación elegante


```python
b[[1, 0, 1, 0],[0, 1, 2, 0]] ### Seleccione los elementos (1,0), (0,1), (1,2) y (0,0)
```




    array([4. , 2. , 6. , 1.5])




```python
b[[1, 0, 1, 0]][:,[0,1,2,0]] ### Seleccione un subconjunto de filas y columnas de la matriz.
```




    array([[4. , 5. , 6. , 4. ],
           [1.5, 2. , 3. , 1.5],
           [4. , 5. , 6. , 4. ],
           [1.5, 2. , 3. , 1.5]])



### Manipulación de Arrays

#### Transposición de matriz


```python
i = np.transpose(b)
```


```python
i.T
```




    array([[1.5, 2. , 3. ],
           [4. , 5. , 6. ]])



#### Cambiar la forma del Array


```python
b.ravel()
```




    array([1.5, 2. , 3. , 4. , 5. , 6. ])




```python
g.reshape(3,-2)
```




    array([[-0.5,  0. ],
           [ 0. , -3. ],
           [-3. , -3. ]])



#### Agregar / eliminar elementos


```python
h.resize((2,6))
```


```python
np.append(h,g)
```




    array([ 1. ,  2. ,  3. ,  0. ,  0. ,  0. ,  0. ,  0. ,  0. ,  0. ,  0. ,
            0. , -0.5,  0. ,  0. , -3. , -3. , -3. ])




```python
np.insert(a, 1, 5)
```




    array([1, 5, 2, 3])




```python
np.delete(a,[1])
```




    array([1, 3])



#### Combinando Array


```python
np.concatenate((a,d),axis=0)
```




    array([ 1,  2,  3, 10, 15, 20])




```python
np.vstack((a,b))
```




    array([[1. , 2. , 3. ],
           [1.5, 2. , 3. ],
           [4. , 5. , 6. ]])




```python
np.r_[e,f]
```




    array([[7., 7.],
           [7., 7.],
           [1., 0.],
           [0., 1.]])




```python
np.hstack((e,f))
```




    array([[7., 7., 1., 0.],
           [7., 7., 0., 1.]])




```python
np.column_stack((a,d))
```




    array([[ 1, 10],
           [ 2, 15],
           [ 3, 20]])




```python
np.c_[a,d]
```




    array([[ 1, 10],
           [ 2, 15],
           [ 3, 20]])



### División de matrices


```python
np.hsplit(a,3) ### Divida la matriz horizontalmente en el tercer índice
```




    [array([1]), array([2]), array([3])]




```python
np.vsplit(c,2) ### Divida la matriz verticalmente en el segundo índice
```




    [array([[[1.5, 2. , 1. ],
             [4. , 5. , 6. ]]]),
     array([[[3., 2., 3.],
             [4., 5., 6.]]])]



### Fin.


```python

```
