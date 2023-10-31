## Taller de Docker - Level 1 - DevOps
### Galo Agustin Arri - Franco Rodriguez
En este archivo, se ecuentra una breve explicacion del compose para levantar un wordpress.

Este archivo yml, es un manifiesto que representa la configuracion de un compose de docker.
Este compose, levanta dos servicios, wordpress y mysql, estan en una red bridge, vinculando el puerto 8080 de nuestro localhost con el 80 del container de wordpress, ademas se crean dos volumenes uno para la base de datos y otro para las paginas de wordpress. Utilizamos variables de entorno, para definir en wordpress, la base de datos que util;iza, el nombre de usuario, contrasenia, y el nombre de la base de datos. Mientras que en el servicio de mysql, definimos las variables del nombre de la base de datos, usuario, contrasenia, y demas variables de entorno necesarias. Por ultimo, en cada contenedor definimos los volumenesde algunas carpetas que se pueden llegar a usarse, de esta manera nos permite, tener un acceso mas comodo a los archivos que se almacenen en dicho directorio. 

En el caso de ser necesario separar o utilizar otro tipo de red, debemos agregar en cada sservicio la "network" que se quiera utilizar. En el caso que esto se cumpla, alfinal del archivo en la seccion de networks, deberemos agregar las redes creadas, con su tipo.


