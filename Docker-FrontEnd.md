# DESPLIEGUE DE APP FRONT-END
1.- Crear Docker-compose
 - Dentro de una instancia, se deve crear una carpeta (fgchillogalli) e ingresar, luego, crear otra carpeta (db) donde estará el back-end e ingresar , dentro de "bd" vanos a crear el archivo "docker-compose.yml"
![Captura de pantalla (710)](https://user-images.githubusercontent.com/91167206/209037064-936c146b-a4da-4287-8c48-3b2c45c881d5.png)

2.- Docker-compose.yml
 - Al crear el archivo docker-compose, debemos especificar la version de los contenedores, nombres, puertos, usuarios, contraseñas, entre otros, para generar el contenedor del pgAdmin y postgres
![Captura de pantalla (711)](https://user-images.githubusercontent.com/91167206/209037873-ea389334-b979-4bb0-a6a2-76383c8e8016.png)

- Una vez creado el archivo, procedemos a ejecutarlo
![Captura de pantalla (712)](https://user-images.githubusercontent.com/91167206/209038012-e352e185-3785-453a-9093-62aa325ab6bd.png)

3.- Crear servidor Postgres
 - Abrimos el puerto 8090 e ingrsamos al pgadmin, una vez dentro creamos un nuevo servidor con los datos detallados para el contenedor postgres
![Captura de pantalla (713)](https://user-images.githubusercontent.com/91167206/209038800-2fe219e4-01c0-47a1-8a33-a04faceceaa3.png)

4.- Git del Back-end
 - En la carpeta "db", debemos clonar el git donde está la app para el back-end para luego editar varios archivos que servirán para la conexión con la base de datos y front-end
![Captura de pantalla (714)](https://user-images.githubusercontent.com/91167206/209039530-3e498145-e2c0-481b-a476-a0cae2d0aa0f.png)

5.- Editar application
 - Vamos a buscar el archivo "application.yml" o "application.properties" para editar los campos de datasource y enableCors
![Captura de pantalla (715)](https://user-images.githubusercontent.com/91167206/209039735-4a5b3b0f-aae1-43dd-933b-dfb130f8dcf5.png)

 - Ahora vamos a editar el datasource con los datos del contenedor Postgres (url, usuario y contraseña), y en el enableCors ponemos la dirección URL del puerto 3000
![Captura de pantalla (716)](https://user-images.githubusercontent.com/91167206/209040113-c308c702-d100-4f99-8c09-283754d1d7a9.png)

6.- Editar Cors del back-end
 - Vamos a buscar el archivo de la configuración de los Cors para editarlo
![Captura de pantalla (717)](https://user-images.githubusercontent.com/91167206/209040421-c512b986-8792-4ab9-b409-78e46bcceed2.png)

 - Una vez dentro del editor del archivo, debemos actualizar la ruta del "allowebOrigins" por la ruta del puerto 3000 del Play with Docker
![Captura de pantalla (718)](https://user-images.githubusercontent.com/91167206/209040732-507deffa-244a-4e0c-9323-927bd596ea54.png)

7.- Editar controlador
 -  Una vez mas debemos buscar el archivo del controlador, ubicado en la carpeta controller y abrirlo con el editor
![Captura de pantalla (719)](https://user-images.githubusercontent.com/91167206/209041268-ecc34a61-f97c-4658-9899-d1d90ae00a85.png)

- Una vez dentro buscaos donde estan los "origins" para actualizar la ruta, por la ruta del puerto 3000 
![Captura de pantalla (720)](https://user-images.githubusercontent.com/91167206/209041637-f17c8531-bc22-4f51-8524-c1a16de8c3e3.png)

8.- Contenedor Maven
 - Para generar el archivo ".jar", antes debemos generar el contenedor maven con el siguiente comando, donde se debe tener en cuenta el nombre de la red de los contenedores y la ubicación del archivo, dado el caso que no escribamos bien el codigo, el contenedor se nos generara de forma erronea
![Captura de pantalla (721)](https://user-images.githubusercontent.com/91167206/209042601-5f150506-3f67-4947-bbcb-b5be8361ef2d.png)

9.- Dockerfile pare el Back-end
 - Dentro de la carpeta principal del git, vamos a crear el archivo "Dockerfile", el cuál nos permite crear la imagen para la app del back-end
![Captura de pantalla (722)](https://user-images.githubusercontent.com/91167206/209045324-03652db2-a9cc-4317-9359-25becf92ff2f.png)

 - Dentro del archivo, vamos ah escribir el siguiente contenido
 ![Captura de pantalla (723)](https://user-images.githubusercontent.com/91167206/209045417-c7f23d2f-ef02-44dc-b514-b1f5f211edb6.png)
 
 10.- Crear imagen y contenedor del Back-end
  - Necesitamos dos comandos para crear tanto la imagen como el contenedor de la app back-end, estos son:
   - "docker build -t nombreImagen ."
   - "docker run -d --name nombreContenedor --network redDeContenedores -p 8081:8081 nombreImagen"
 - Luego de haber ejecutado los dos comandos, se creará el puerto 8081, el cuál es la conexión con la base de datos
 
 




