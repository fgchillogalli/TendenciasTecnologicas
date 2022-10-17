# TendenciasTecnologicas
#Practica En Docker

#Para iniciar en Docker lo primero es crearnos una cuenta de Docker Hub
![Captura de pantalla (634)](https://user-images.githubusercontent.com/91167206/196086242-fbd9f2f2-c342-41bf-83ef-c37a8d93a008.png)

#Una vez creada la cuenta y confirmado nuestro correo, buscamos en Google "Play With Docker" 
![Captura de pantalla (635)](https://user-images.githubusercontent.com/91167206/196086756-ee514bae-26d9-4bde-ba70-4e488255978e.png)

#Procedemos a Logearnos con Docker y Damos Start
![Captura de pantalla (636)](https://user-images.githubusercontent.com/91167206/196086974-caf82079-80a3-4666-a60a-537e081ac592.png)

#Si no nos carga la pagina a la primera lo que hacemos es retroceder y volver a darle a Start hasta que nos la pagina siguiente
![Captura de pantalla (637)](https://user-images.githubusercontent.com/91167206/196087104-97ee1b86-fbad-4101-9232-669f5a73b3d0.png)

#Aqui podemos realizar varias practicas, como crear un contenedor, que es lo que vamos a realizar a continuacion

#Para ello vamos a "ADD NEW INSTANCE"

#Seguido obtendremos una pantalla en donde vamos a poder ingresar comandos, dependiendo de lo que necesitemos
![Captura de pantalla (638)](https://user-images.githubusercontent.com/91167206/196087502-0c0f08ab-9327-4bd2-923a-5e0bcb0316e1.png)

#Aqui vamos a introducir el siguiente codigo "docker run --name "Practicas" -p 80:80 -d nginx"

#Explicando el codigo:

#docker run = sirve para iniciar y crear un contenedor

#--name "nombre"= Ponemos un nombre a nuestro contenedor por ejemplo (Practicas)

#-p = Agregamos los puertos, el de la izquierda es el puerto de la maquina anfitriona y el de la derecha el del servidor a usar

#-d = Recuperamos el ($), impide que el codigo se siga ejecutando.

#nginx = Imagen del contenedor, (En base ha esta se creara el contenedor)

#De esta manera se iniciaran varias descargar y nuestro contenedor sera creado.
![Captura de pantalla (639)](https://user-images.githubusercontent.com/91167206/196088110-f9110d5e-a87e-40ce-a044-d3b02ac67ffd.png)

#Para poder listar y ver el estado de nuestros contenedores utilizamos el comando "docker ps"
![Captura de pantalla (640)](https://user-images.githubusercontent.com/91167206/196089369-2acb91b9-0aed-45a3-8cd1-676a600ea4be.png)
