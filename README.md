# Tarea03_SXE_Docker

Esta práctica fue realizada en Windows.

## 1. Descarga la imagen "alpine" SIN ARRANCARLA y comprueba que está en tu equipo.

```bash
docker pull alpine 
docker images
````
Con 'pull' se descarga la imagen e 'images' muestra las que están en nuestro equipo.

![1.PNG](img%2F1.PNG)

---

## 2. Crea un contenedor sin ponerle nombre. ¿está arrancado? Obtén el nombre

**Comandos:**
```bash
docker create alpine  
docker ps 
docker ps -a 
````
Creamos el contenedor con 'create alpine'. Este comando solo crea el contenedor, 
no lo arranca. Por eso 'ps' (que solo muestra los contenedores en ejecución) no lo lista. 
Usamos docker 'ps -a' para ver todos los contenedores y obtener el nombre aleatorio que se le asignó automáticamente.

![2.PNG](img%2F2.PNG)

---

## 3. Crea un contenedor con el nombre 'dam_alp1'. ¿Como puedes acceder a él?

**Comandos:**
```bash
docker run -it --name dam_alp1 alpine 
````
Lo creamos y entramos en el a la vez. '-- name' nos permite asignarle un nombre.

![3.PNG](img%2F3.PNG)

---

## 4. Comprueba que ip tiene y si puedes hacer un ping a google.com

**Comandos:**
```bash
ip a  muestra ip
ping -c 4 google.com para hcer ping a google
````
Con 'ip a' mostramos la IP de dam_alp1 y con 'ping' comprobamos que podemos hacer ping a google.com.

![4.PNG](img%2F4.PNG)

---

## 5. Crea un contenedor con el nombre 'dam_alp2'. ¿Puedes hacer ping entre los contenedores?

**Comandos:**
```bash
docker run -it --name dam_alp2 alpine
ping -c 4 172.17.0.2
````
Creamos otro contenedor de la misma forma que el anterior. Y comprobamos que hacen ping entre ellas.

![5.PNG](img%2F5.PNG)

----

## 6. Sal del terminal, ¿que ocurrió con el contenedor?

**Comandos:**
```bash
Exit para salir de la terminal
ps -a  muestra que el estado de dam_alp1 y dam_alp2 es exited. 
````
Salimos de la terminal con 'exit' y con 'ps -a' comprobamos que el estado del contenedor.

![6.PNG](img%2F6.PNG)

---

## 7. Cuanta memoria en el disco duro ocupaste

**Comandos:**
```bash
docker images muestra el tamaño de las imagenes
docker system df muestra todo lo que ocupa docker
````
'images' muestra solo informacion de las imagenes y 'system df' muestra la informacion de todo docker.

![7.PNG](img%2F7.PNG)

---

## 8. Cuanta RAM ocupan los contenedores? ¿Hay algún comando docker para saber esto?.

**Comandos:**
```bash
docker stats
````
En el apartado *MEM USAGE* se muestra la memoria RAM que se utiliza.

![8.PNG](img%2F8.PNG)

