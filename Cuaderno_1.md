## Configuracion de ANACONDA con Jupyter Notebook



1. Descargar el instalador y ejecutable de ANACONDA en el sitio oficial [Descargar Anaconda](https://www.anaconda.com/products/individual)


2. Ejecutar el instalador de ANACONDA, recomendacion ejecutar como administrador ![image.png](attachment:image.png)


3. Al elegir dónde instalar el software en la pestaña "Seleccionar destino", seleccione Instalar solo para mí "Just me (recommended)" . De lo contrario, necesitará acceso de administrador para realizar actualizaciones y acceder a algunos elementos desde la línea de comandos. Además, es una buena práctica de seguridad instalar solo localmente.
 ![image-2.png](attachment:image-2.png)


4. Seleccione la ubicación de instalación para Anaconda ( puede seleccionar el valor predeterminado del disco local C u otra ubicación personalizada, debe ser ubicación fija). Haga clic en Siguiente cuando esté listo para continuar. 


5. Haga clic en la casilla de verificación para registrar Anaconda como su Python predeterminado. No agregue Anaconda a su variable PATH. ![image-3.png](attachment:image-3.png)


6. Haga click en instalar para iniciar la instalación de ANACONDA. ![image-4.png](attachment:image-4.png)


7. Una vez finalizada la instalación, no elija instalar PyCharm IDE. Usaremos Jupyter Lab en este curso y PyCharm no será compatible. ![image-5.png](attachment:image-5.png)


8. Verifique que la instalación sea exitosa iniciando Anaconda Navigator desde su menú de inicio.
![image-6.png](attachment:image-6.png)


## Uso de paquetes predeterminados en Jupyter Notebook

a. Explore e investigue que paquetes se integran con la instalación de Jupyter notebook de Anaconda.
    ![image.png](attachment:image.png)
    
b. Estructura de un cuaderno de Jupyter Notebook.
      
   #### - ¿ Como esta dividido un cuaderno de Jupyter Notebook ?
      
###### El cuaderno Jupyter consta de tres componentes
###### La aplicación web del cuaderno: 
Para escribir y ejecutar código en un entorno interactivo.
###### Núcleos:
Kernel es un motor de cálculo que ejecuta el código de los usuarios presente en el documento del cuaderno en un idioma determinado y devuelve la salida a la aplicación web del cuaderno. El kernel también se ocupa de cálculos para widgets interactivos, introspección y finalización de pestañas.
###### Documentos de cuaderno:
Un documento es una representación de todo el contenido visible en la aplicación web del cuaderno. Esto incluye entrada y salida de cálculos, gráficos, texto narrativo, widgets interactivos, ecuaciones, imágenes y video. Hay un kernel separado para cada documento. Los documentos del cuaderno se pueden convertir a varios formatos y compartir entre otros mediante el correo electrónico, Dropbox y herramientas de control de versiones como git.

![image-2.png](attachment:image-2.png)

   #### - ¿ Como ejecutar codigo ?
       
   ###### Para ejecutar la celda, necesitamos agregar algo a la celda.

La celda puede contener las declaraciones escritas en un lenguaje de programación del kernel actual. Elegimos el kernel cada vez que creamos un nuevo cuaderno. Recuerde que creamos un cuaderno que elegimos Python 3. Eso significa que nuestra celda puede contener un código Python. El boton de ejecutar se encuentra en la parte superior del menu.
![image-4.png](attachment:image-4.png) ![image-5.png](attachment:image-5.png)

La forma alternativa de ejecutar una celda es, en su teclado, simplemente presione Shift + Enter. La salida deberia verse asi.

![image-3.png](attachment:image-3.png)

   #### - Exportar a formatos estaticos como Markdown, HTML y PDF.
        
![image-6.png](attachment:image-6.png)


### Instalacion de paquetes adicionales recomendados.


  ###### a-  Instalacion de paquetes usando Anaconda.
          
           conda install <NOMBRE_PAQUETE>
           
  ######         Instalación de paquetes usando pip
  
           pip install <NOMBRE_PAQUETE>


##### Instale los siguientes paquetes que se relacionan a la inteligencia artificial

- scikit-learn
- pandas
- numpy
- tensorflow-gpu (si no tiene GPU use solo tensorflow)
- pytorch


![descarga%202.JPG](attachment:descarga%202.JPG)


![scikit-learn.JPG](attachment:scikit-learn.JPG)
![scikit-learn.JPG](attachment:scikit-learn.JPG)
