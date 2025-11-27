**ROS 2** es un marco de software diseñado para construir robots y **sistemas robóticos** de forma modular, flexible y distribuida.  
En lugar de crear un único programa monolítico que contenga todo (sensores, controladores, lógica, actuadores), con ROS 2 estructuramos la lógica del robot como una **red de componentes independientes** que se comunican entre sí de forma organizada.
Este enfoque **modular** permite dividir las responsabilidades del sistema en partes pequeñas, especializadas y autónomas. Cada parte puede desarrollarse, probarse y modificarse por separado, lo que facilita enormemente el desarrollo, mantenimiento, extensión y reutilización del código.

# Componentes clave de un sistema ROS 2

Un sistema típico con ROS 2 se basa en varios conceptos fundamentales — cada uno con un rol específico — que, combinados, permiten la comunicación y coordinación entre los distintos módulos del robot:

- **Nodos**: unidades independientes de ejecución, encargadas de tareas específicas: leer sensores, controlar motores, procesar datos, lógica de decisión, etc.  
- **Tópicos (Topics)**: canales de comunicación mediante los cuales los nodos pueden enviar o recibir información. Por ejemplo: datos de sensores, estados, comandos.  
- **Servicios (Services)**: mecanismo de comunicación para operaciones puntuales o solicitudes-respuesta. Útil para tareas discretas como pedir un cálculo, resetear un estado, cambiar un parámetro, etc.  
- **Visualización / introspección (rqt / rqt_graph)**: cuando el sistema tiene muchos nodos y comunicaciones, estas herramientas gráficas permiten “ver” el grafo del sistema: nodos, conexiones, flujo de datos — lo que ayuda a entender, depurar y documentar la arquitectura.

# Ventajas de esta arquitectura modular

- **Orden y claridad**: cada módulo tiene una responsabilidad claramente definida. Esto reduce la complejidad y facilita el mantenimiento.  
- **Flexibilidad y reutilización**: puedes reutilizar nodos en distintos proyectos, o reemplazar partes del sistema sin afectar lo demás.  
- **Escalabilidad**: el mismo enfoque sirve para proyectos simples (un sensor, un motor) o complejos (robot con múltiples sensores, control, visión, planificación).  
- **Distribución**: los nodos pueden correr en la misma máquina o en máquinas distintas — ideal para sistemas con hardware heterogéneo, carga distribuida o integración de múltiples subsistemas.  
- **Depuración y documentación más sencilla**: con la visualización del grafo y la separación modular, puedes entender cómo fluye la información, detectar errores o conflictos, y documentar de forma clara tu arquitectura.

Orden a aprender:
- Nodos
- Topicos
- Servicios
- Visualización rqt