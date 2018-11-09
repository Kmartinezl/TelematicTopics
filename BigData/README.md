## EJECUCIÓN DEL PROYECTO
 
 Para poder visualizar el proyecto, es necesario tener primero el ambiente configurado:
 * Primero vamos a descargar un ambiente de virtualización como VMware o VirtualBox. Para los siguientes ejemplos pasos vamos a estar utilizando VirtualBox:
    https://www.virtualbox.org/wiki/Downloads
 * Ahora vamos a descargar e instalar Vagrant: 
    https://www.vagrantup.com
Recuerda descargar la versión segun el sistema operativo en el que estés trabajando.

* Ahora procedemos a clonar o descargar la aplicación : 
* Nos dirigimos a la carpeta del proyecto y ejecutamos el siguiente comando:
  ```
  vagrant up 
  ``` 
 Esto puede tomar algún tiempo segun la velocidad de red de la que disponga. 
 
 * Después de todo esté listo, vamos a entrar a la máquina virtual a través del ssh provisto por Vagrant: 
    ```
    vagrant ssh
    ``` 
 
 * Nos cercioramos de que sí estemos en la máquina virtual y no en nuestra máquina y ejecutamos el siguiente comando: 
 
    ```
    mvn clean
    ``` 
    
Van a aparecer una serie de descargas que tomarán aproximadamente de 1-2 min según la velocidad de la red. 

* Una vez que aparezca el mensaje _Build success_ , ejecutamos por último el siguiente comando: 

   ```
   mvn package
   ``` 
   
* Nos dirigimos a Vagrant/viz y ejecutamos el comando:
    ```
    python app.py
    ```

Ahora en nuestro navegador de preferencia y abrimos http://127.0.0.1:5000  para poder ver la aplicación ejecutando.
 
