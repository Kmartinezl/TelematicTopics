# Documento de análisis
## Data Streaming desde twitter






#### Alejandro Velasquez Uribe
#### Keila Andrea Martínez Lagares
#### 21 de octubre de 2018







#### Universidad EAFIT
#### ST0263 – Tópicos especiales en Telemática
#### Edwin Montoya
-----------------------------------------------------------------------------------------------------------------------------

**1. Problema a resolver:**
Análisis de Sentimientos usando Data Streaming desde Twitter con Kafka y Spark.

Lo que se busca hacer con esta aplicación es analizar los Tweets de diferentes usuarios para saber su  posición frente a un tema, estas posiciones pueden ser positivas, negativas o neutras.

**2. Arquitectura preliminar de datos:**

* **Ciclo de vida:**
Businses question,
Data source,
Data ingestion,
Data storage,
Data processing and analytics,
Data app (visualization IE).

* **Procesamiento:** Los datos, al comportarse como transmisión, son procesados con un producto de transmisión llamado Apache Spark Streaming.

* **Almacenamiento:** Memoria


**3. Fuentes y naturaleza de los datos:**

Los datos son provisionados directamente desde la plataforma de Twitter usando su API, pero usamos un módulo de Phyton llamado Tweepy el cual nos ayuda a comunicarnos desde Phyton con la plataforma de Twitter y usar su API.
 
* **Tecnologías a utilizar:**  Tweepy, Twitter streaming API, Phyton.


**4. Sistema de ingesta de datos:**

Una vez que leamos los datos desde Twitter, estos son enviados a Kafka topic usando Kafka producer, Usamos Kafka ya que es usado para hacer tuberías(pipelines) de datos en streaming  y aplicaciones de streaming
            
* **Tecnologías a utilizar:**  Kafka


**5. Almacenamiento de los datos:**
La transmisión de datos solo tiene valor cuando esta es en vivo, es por eso que almacenar los datos permanentemente en algún lugar como Hadoop sería inútil. 
Los datos escritos en Kafka se escriben en el disco y se replican para obtener tolerancia a fallos. Kafka permite a los productores esperar el reconocimiento para que una escritura no se considere completa hasta que esté completamente replicada y se garantice que persiste incluso si el servidor escrito falla.


* **Tecnologías a utilizar:** Kafka.


**6. Análisis de datos:**
Usaremos el componente de Spark Streaming el cual nos permite procesar data en     tiempo real, como toda la data entra en memoria el proceso de análisis es mucho más rápido, además de que podemos computar todo esto en paralelo. 
* **Tecnologías a utilizar:**  Apache Spark.          
