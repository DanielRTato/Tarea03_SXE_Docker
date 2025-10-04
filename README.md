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