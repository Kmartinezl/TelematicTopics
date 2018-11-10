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
Contador de las palabras mas utilizadas en twitter.

Lo que se busca hacer con esta aplicación es analizar los Tweets de diferentes usuarios para saber que palabras son las que se usan mas frecuentemente en twitter, ademas de podes obsevar patrones top trending.

**2. Arquitectura preliminar de datos:**

* **Ciclo de vida:**
Businses question,
Data source,
Data storage,
Data processing and analytics,
Data app (visualization IE).

* **Procesamiento:** Los datos, al comportarse como transmisión, son procesados con un producto de transmisión llamado storm.

* **Almacenamiento:** Aunque los datos son analizados en tiempo real son almacenados temporalmente en Redis Database ya que esta base de datos guarda los elementos en memoria.


**3. Fuentes y naturaleza de los datos:**

Los datos son provisionados directamente desde la plataforma de Twitter usando su API, al ser estos datos tweets, obtenidos por medio de streaming (tiempo real), obtrendremos datos como recomendaciones, búsquedas o tendencias en la red, dichos datos son cadenas de caracteres que posteriormente son tratados como tuplas.
 
* **Tecnologías a utilizar:**   Twitter streaming API, Java, y Storm paara el procesamiento de los datos.
.

**4. Sistema de ingesta de datos:**

Apache storm es el que recopila y analiza en tiempo real.
            
* **Tecnologías a utilizar:**  Storm


**5. Almacenamiento de los datos:**
Aunque el procesamiento de los datos en tiempo real, estamos utilizando Redis Database para su almacenamiento.

* **Tecnologías a utilizar:** Redis Database


**6. Análisis de datos:**
Usaremos el componente de Apache Storm el cual nos permite procesar data en tiempo real, como toda la data entra en memoria el proceso de análisis es mucho más rápido, además de que podemos computar todo esto en paralelo. 
* **Tecnologías a utilizar:**  Apache Storm.          
