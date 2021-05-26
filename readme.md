# Lab 1 - Conexión al cluster
El presente repositorio cuenta con toda la documentación para la realizacion del Lab 1 - Conexión al cluster de la materia Tópicos especiales en telemática ST0263-002

**Santiago Hincapié Murillo**

*20172002001*

shincapiem@eafit.edu.co

## Definiciones
- Un **clúster** se aplica a los [**sistemas distribuidos**](https://es.wikipedia.org/wiki/Computaci%C3%B3n_distribuida) de granjas de computadoras unidas entre sí comúnmente por una red de alta velocidad y que se comportan como si fuesen un único servidor. 

- Un [**EMR**](https://docs.aws.amazon.com/es_es/emr/latest/ManagementGuide/emr-what-is-emr.html) es una plataforma de clúster administrada que simplifica la ejecución de los marcos de trabajo de [**Big Data**](https://www.powerdata.es/big-data#:~:text=Cuando%20hablamos%20de%20Big%20Data,convencionales%2C%20tales%20como%20bases%20de) en AWS para procesar y analizar grandes cantidades de datos. 

- **Hadoop** es una estructura de software de código abierto para almacenar datos y ejecutar aplicaciones en clústeres de hardware comercial. Proporciona almacenamiento masivo para cualquier tipo de datos, enorme poder de procesamiento y la capacidad de procesar tareas o trabajos concurrentes virtualmente ilimitados. [Fuente](https://www.sas.com/es_co/insights/big-data/hadoop.html#:~:text=Hadoop%20es%20una%20estructura%20de,o%20trabajos%20concurrentes%20virtualmente%20ilimitados.)


## Creación del clúster en AWS
En la imagen se aprecia *emr-5.33.0* pero se tomó la versión *emr-6.1.0* para realizar este laboratorio.

![1](https://github.com/AltoSolid/lab1-Telematica/blob/main/Img/Creacion-Cluster/uno.png)


Se continua con la selección de las máquinas a continuación (esto para tener un menor costo por el uso de recursos menos "potentes").

![2](https://github.com/AltoSolid/lab1-Telematica/blob/main/Img/Creacion-Cluster/dos.png)


Ahora en siguiente y vemos la opción de Security group y seleccionamos la clave que ya creamos posteriormente en *key pair* para este laboratorio.

![3](https://github.com/AltoSolid/lab1-Telematica/blob/main/Img/Creacion-Cluster/tres.png)


La siguiente información la dejamos tal cual se encuentra.

![4](https://github.com/AltoSolid/lab1-Telematica/blob/main/Img/Creacion-Cluster/cuatro.png)


Al crear el clúster esperaremos a que inicie el mismo:

![5](https://github.com/AltoSolid/lab1-Telematica/blob/main/Img/Creacion-Cluster/cinco.png)


Luego de ser creado correctamente, debe de rellenarse el circulo en color verde y al ingresar a él, podremos ver información como la siguiente: 

![6](https://github.com/AltoSolid/lab1-Telematica/blob/main/Img/Creacion-Cluster/cinco.png)


## Gestión de los archivos con Hue en Amazon EMR
Continuaremos primero a revisar en *Security Groups* y añadiremos dos reglas en el puerto 22 y el 8888:

![sg1](https://github.com/AltoSolid/lab1-Telematica/blob/main/Img/security-group1.png)

![sg](https://github.com/AltoSolid/lab1-Telematica/blob/main/Img/security-group.png)

Ahora procederemos a trabajar con **Hue**

![1](https://github.com/AltoSolid/lab1-Telematica/blob/main/Img/HUe/uno.png)

![2](https://github.com/AltoSolid/lab1-Telematica/blob/main/Img/HUe/dos.png)

![3](https://github.com/AltoSolid/lab1-Telematica/blob/main/Img/HUe/tres.png)

![4](https://github.com/AltoSolid/lab1-Telematica/blob/main/Img/HUe/cuatro.png)


## Gestión con SSH por la consola
Conexión a la máquina *master*

![1](https://github.com/AltoSolid/lab1-Telematica/blob/main/Img/SSH/uno.png)

Se ejecutarán los siguientes comandos con los resultados:

![2](https://github.com/AltoSolid/lab1-Telematica/blob/main/Img/SSH/dos.png)

![3](https://github.com/AltoSolid/lab1-Telematica/blob/main/Img/SSH/tres.png)

![4](https://github.com/AltoSolid/lab1-Telematica/blob/main/Img/SSH/cuatro.png)

![5](https://github.com/AltoSolid/lab1-Telematica/blob/main/Img/SSH/cinco.png)

![6](https://github.com/AltoSolid/lab1-Telematica/blob/main/Img/SSH/seis.png)

![7](https://github.com/AltoSolid/lab1-Telematica/blob/main/Img/SSH/siete.png)
