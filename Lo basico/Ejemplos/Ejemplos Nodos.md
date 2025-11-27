# Ejemplos Nodos

Cuando instalamos Ros2 este viene con un paquete llamado "turtlesim" y para ejecutarlo desde su paquete sería:

```bash
ros2 run turtlesim turtlesim_node
```
Se te abrirá una ventana con una tortuga en el centro y para poder moverla necesitaras correr en otra terminal el nodo que te permite controlarla con las flechas de tu pc que se encuentra en la misma carpeta de turtlesim

```bash
ros2 run turtlesim turtle_teleop_key
```
Para ver la cantidad de nodos abiertos en tu sistema podrás ejecutar en una nueva terminal:

```bash
ros2 node list
```
El cual te mostrará que los unicos 2 nodos abiertos que tienes de momento. También si quieres obtener mas información de algun nodo puedes correr por ejemplo:

```bash
ros2 node info /turtlesim
```
Que te arrojará todos los detalles de este nodo


Otro punto a recalcar son los nombres, remapeo y modularidad de nodos.
Los nombres de los nodos no son fijos ya que cambian constantemente, pero puedes especificarles un nombre unico y distinto para que cuando necesites buscarlo en alguna lista o grafica puedas encontrarlo
Para ello aqui tienes un ejemplo:

```bash
ros2 run turtlesim turtlesim_node --ros-args --rema __node:=my_turtle
```
Si mantenias abierto el turtlesim anterior, se te abrirá una nueva ventana (asi que toma este codigo como un ejecutable más nombre) y cuando revises la lista de nodos verás uno nuevo con el nombre de "my_turtle" aparte del que ya tenías

# Ya pero, por qué es importante eso?

Si tu robot tiene muchos componentes los noddos te permiten estructurar todo esto de forma clara y ordenada. Sobre toddo con los comandos de inspeccion "node list, node info" podras buscarlos facilmente aún más cuando los remapeas y les das un nombre unico.
Porque imaginate que tuvieras 5 sensores diferentes, cada uno para una tarea especifica y estos se tienen que comunicar entre si y los debes de configurar uno por uno, ahi entran los nodos que los separa y nos lleva al siguiente tema que son los Topicos.