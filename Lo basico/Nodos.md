# NODOS

Un sistema robótico completo se compone de muchos nodos, los cuales cada uno tendra una funcion determinada por el usuario y estos pueden intercambiar información.

Entonces podemos decir que un nodo es:
- La unidad computacional mas básica de un proceso (Sensor, Actuador, Procesar información, etc.)
- Importante que cada nodo tenga una unica responsabilidad, clara y bien echa
- Estos se pueden almacenar en un mismo ejecutable.

# Comandos

Para correr un ejecutable dentro de un paquete

```bash
ros2 run <package_name> <executable_name>
```
Donde "<package_name>" es el nombre de la carpeta o paquete y "<executable_name>" es el nombre del nodo o ejecutable dentro de esa carpeta o paquete

Para ver la lista de nodos corriendo dentro el sistema:

```bash
ros2 node list
```

Ver los detalles de un nodo en especifico:

```bash
ros2 node info <node_name>
```
Esto nos permitirá ver a qué topico está publicando o suscribiendo su información

# Puedes ver los ejemplos de nodos ahora