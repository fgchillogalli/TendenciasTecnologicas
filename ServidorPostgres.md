# Servidor Postgres

***Para crear un servidor con postgres, vamos ha usar los siguientes comandos:

***docker run: inicia docker

***-d: terminar la ejecucion

***--name: Nombre del contenedor de postgres

***-e: variable de entorno para el usuario Postgres

***-p: puerto del anfitrion y del contenedor

***postgres: nombre de la imagen
![Captura de pantalla (659)](https://user-images.githubusercontent.com/91167206/201255380-a434cfe4-fa27-4bf3-bcec-a29cf1376780.png)

***Una vez creado la base con postgress, procedemos a crear una cuenta en Pgadmin con el siguiente comando, en donde configuraremos el puerto en este caso 8090:80 nuestro correo y una contraseña
![Captura de pantalla (660)](https://user-images.githubusercontent.com/91167206/201255889-f0233246-7a1a-468a-a5e9-b26a74584c7b.png)
*** Una vez creada la cuenta, verificamos abriendo el localhost: 8090
![Captura de pantalla (661)](https://user-images.githubusercontent.com/91167206/201256107-ac7b634f-8018-483d-9255-1401e080f399.png)
![Captura de pantalla (662)](https://user-images.githubusercontent.com/91167206/201256354-eb2999d6-cd01-4daf-9a61-9e6e422f0b7d.png)

***Una vez verificada que se abara el puerto y nuestra cuenta este activa, procedemos a configurar la red con el siguiente comando "redbimbo" puede cambiar por el nombre de la red de su preferencia:
![Captura de pantalla (664)](https://user-images.githubusercontent.com/91167206/201256590-0bb5888e-c757-419a-a047-e3cbe5c57fd8.png)

***Luego de que ya tengamos creada la red, procedemos a agregar los contenedores
***Agregando contenedor postgress con el siguiente codigo:
![Captura de pantalla (665)](https://user-images.githubusercontent.com/91167206/201257005-25f7bb97-8e78-4d2c-8d96-93e295431868.png)

***Ahora agregamos el contenedor de PGadmin: 
![Captura de pantalla (666)](https://user-images.githubusercontent.com/91167206/201257096-51d0e102-1a2c-435d-962d-a9ff8199d44b.png)

***Una vez ya agregados los contenedores vamos a verificar que todo este correcto, para lo cual usamos el sigueinte codigo, el cual mostrata las Ips que fueron asiganadas a cada contenedor
![Captura de pantalla (667)](https://user-images.githubusercontent.com/91167206/201257299-f0a9302b-8adf-4e30-b3c5-7491eda5a508.png)
![Captura de pantalla (668)](https://user-images.githubusercontent.com/91167206/201257296-711fd1a4-be94-47a7-8655-2dd7150c52a2.png)
![Captura de pantalla (669)](https://user-images.githubusercontent.com/91167206/201257295-e24530e5-3c7f-47aa-956d-7991b204bf20.png)
![Captura de pantalla (670)](https://user-images.githubusercontent.com/91167206/201257293-945519f8-bd9b-42ea-92cc-a4f184ddaab5.png)


