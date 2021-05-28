# Lab 2 - Spark
El presente repositorio cuenta con toda la documentación para la realizacion del Lab 2 - Spark de la materia Tópicos especiales en telemática ST0263-002

**Santiago Hincapié Murillo**

*20172002001*

shincapiem@eafit.edu.co

## 1. De forma interactiva vía Spark (En el nodo Master de EMR o en )
Primero nos conectamos vía Spark al nodo Master como se muestra a continuación:
![Spark-1]()
![Spark-2]()

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
![Spark-3]()
![Spark-4]()
![Spark-5]()


## Zeppelin Notebook 
Ingresamos a *https://hdpzeppelin.dis.eafit.edu.co*

Y procedemos a loguearnos y a ejecutar los siguientes pasos: 
![zeppelin-1]()
![zeppelin-2]()
![zeppelin-3]()
![zeppelin-4]()
![zeppelin-5]()
![zeppelin-6]()

## Jupyter Notebook en EMR
1. Clonamos el Cluster del lab1
2. Creamos un notebook 
3. Copiamos las lineas en el notebook nuevo,
4. Ejecutamos el notebook paso a paso
![1]()
![2]()
![3]()
![4]()
![5]()
![6]()
![7]()
![8]()
![9]()

