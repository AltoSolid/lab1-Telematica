# Lab 2 - Spark
El presente repositorio cuenta con toda la documentación para la realizacion del Lab 2 - Spark de la materia Tópicos especiales en telemática ST0263-002

**Santiago Hincapié Murillo**

*20172002001*

shincapiem@eafit.edu.co

## 1. De forma interactiva vía Spark (En el nodo Master de EMR o en )
Primero nos conectamos vía Spark al nodo Master como se muestra a continuación:

![Spark-1](https://github.com/AltoSolid/lab1-Telematica/blob/main/lab2/Img/Spark-1.png)

![Spark-2](https://github.com/AltoSolid/lab1-Telematica/blob/main/lab2/Img/Spark-2.png)


Ahora corremos el siguiente comando: 

    $ pyspark
    >>> files_rdd = sc.textFile("hdfs:///datasets/gutenberg-small/*.txt")
    >>> wc_unsort = files_rdd.flatMap(lambda line: line.split()).map(lambda word: (word, 1)).reduceByKey(lambda a, b: a + b)
    >>> wc = wc_unsort.sortBy(lambda a: -a[1])
    >>> for tupla in wc.take(10):
    >>>     print(tupla)
    >>> wc.saveAsTextFile("hdfs:///tmp/<your-username>wcout1")

    * asi salva wc un archivo por rdd.
    * si quiere que se consolide en un solo archivo de salida:

    $ pyspark
    >>> ...
    >>> ...
    >>> wc.coalesce(1).saveAsTextFile("hdfs:///tmp/<your-username>wcout2")


Se mostraría como se aprecia a continuación: 

![Spark-3](https://github.com/AltoSolid/lab1-Telematica/blob/main/lab2/Img/Spark-3.png)

![Spark-4](https://github.com/AltoSolid/lab1-Telematica/blob/main/lab2/Img/Spark-4.png)

![Spark-5](https://github.com/AltoSolid/lab1-Telematica/blob/main/lab2/Img/Spark-5.png)


## Zeppelin Notebook 
Ingresamos a *https://hdpzeppelin.dis.eafit.edu.co*

Y procedemos a loguearnos y a ejecutar los siguientes pasos: 

![zeppelin-1](https://github.com/AltoSolid/lab1-Telematica/blob/main/lab2/Img/Zeppelin/Zeppelin-1.png)

![zeppelin-2](https://github.com/AltoSolid/lab1-Telematica/blob/main/lab2/Img/Zeppelin/Zeppelin-2.png)

![zeppelin-3](https://github.com/AltoSolid/lab1-Telematica/blob/main/lab2/Img/Zeppelin/Zeppelin-3.png)

![zeppelin-4](https://github.com/AltoSolid/lab1-Telematica/blob/main/lab2/Img/Zeppelin/Zeppelin-4.png)

![zeppelin-5](https://github.com/AltoSolid/lab1-Telematica/blob/main/lab2/Img/Zeppelin/Zeppelin-5.png)

![zeppelin-6](https://github.com/AltoSolid/lab1-Telematica/blob/main/lab2/Img/Zeppelin/Zeppelin-6.png)

## Jupyter Notebook en EMR
1. Clonamos el Cluster del lab1
2. Creamos un notebook 
3. Copiamos las lineas en el notebook nuevo,
4. Ejecutamos el notebook paso a paso

![1](https://github.com/AltoSolid/lab1-Telematica/blob/main/lab2/Img/Notebook/1.png)

![2](https://github.com/AltoSolid/lab1-Telematica/blob/main/lab2/Img/Notebook/2.png)

![3](https://github.com/AltoSolid/lab1-Telematica/blob/main/lab2/Img/Notebook/3.png)

![4](https://github.com/AltoSolid/lab1-Telematica/blob/main/lab2/Img/Notebook/4.png)

![5](https://github.com/AltoSolid/lab1-Telematica/blob/main/lab2/Img/Notebook/5.png)

![6](https://github.com/AltoSolid/lab1-Telematica/blob/main/lab2/Img/Notebook/6.png)

![7](https://github.com/AltoSolid/lab1-Telematica/blob/main/lab2/Img/Notebook/7.png)

![8](https://github.com/AltoSolid/lab1-Telematica/blob/main/lab2/Img/Notebook/8.png)

![9](https://github.com/AltoSolid/lab1-Telematica/blob/main/lab2/Img/Notebook/9.png)

![10](https://github.com/AltoSolid/lab1-Telematica/blob/main/lab2/Img/Notebook/10.png)

## Comprobación: 

![10](https://github.com/AltoSolid/lab1-Telematica/blob/main/lab2/Img/Notebook/11.png)