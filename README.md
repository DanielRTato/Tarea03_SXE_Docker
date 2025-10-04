# Tarea03_SXE_Docker
Tarea 03 de SXE

1. Descarga la imagen "alpine" SIN ARRANCARLA y comprueba que está en tu equipo.

Comandos:

docker pull alpine descarga la imagen

docker images ls para mostrar las imagenes en el equipo

![1.PNG](img%2F1.PNG)

---

2. Crea un contenedor sin ponerle nombre. ¿está arrancado? Obtén el nombre

Comandos:
- docker create alpine para crearlo 
- No no está arrancada porque con docker ps no se muestra (muestra solo los contenedores activos)
- docker ps -a para mostrar todas. y asi consigo el nombre, que es aleatorio (loving_shannon)

![2.PNG](img%2F2.PNG)

---

3. Crea un contenedor con el nombre 'dam_alp1'. ¿Como puedes acceder a él?

Comandos:

docker run -it --name dam_alp1 alpine lo crea y entra la vez

![3.PNG](img%2F3.PNG)

---

4. Comprueba que ip tiene y si puedes hacer un ping a google.com

Comandos:

ip a  muestra ip

ping -c 4 google.com para hcer ping a google

![4.PNG](img%2F4.PNG)

---

5. Crea un contenedor con el nombre 'dam_alp2'. ¿Puedes hacer ping entre los contenedores?

Comandos:

docker run -it --name dam_alp2 alpine

ping -c 4 172.17.0.2

Sí, pueden hacer ping entre ellos

![5.PNG](img%2F5.PNG)

6. Sal del terminal, ¿que ocurrió con el contenedor?

Comandos:

Exit para salir de la terminal

ps -a  muestra que el estado de dam_alp1 y dam_alp2 es exited. 
El contenedor se detiene.

![6.PNG](img%2F6.PNG)

---

7. Cuanta memoria en el disco duro ocupaste

Comandos:

docker images muestra el tamaño de las imagenes

docker system df muestra todo lo que ocupa docker

![7.PNG](img%2F7.PNG)

---

8. Cuanta RAM ocupan los contenedores? ¿Hay algún comando docker para saber esto?.

Comando:

docker stats

EN el apartado MEM USAGE se muestra la memorai que está utilizando cada contenedor

![8.PNG](img%2F8.PNG)

