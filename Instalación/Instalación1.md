# Esquema basado de
 https://docs.ros.org/en/jazzy/index.html

## Paso 1
Nos aseguraremos de que nuestro entorno de trabajo esté configurado correctamente y soporte el lenguaje.  
Para esto ejecutaremos el siguiente comando en una terminal:

```bash
locale  # check for UTF-8
sudo apt update && sudo apt install locales
sudo locale-gen en_US en_US.UTF-8
sudo update-locale LC_ALL=en_US.UTF-8 LANG=en_US.UTF-8
export LANG=en_US.UTF-8

locale  # verify settings
```
Ahora añadiremos el repositorio ROS2 apt a nuestro sistema, pero antes de eso tenemos que asegurarnos que el repositorio Ubuntu Universe esté habilitado.

```bash
sudo apt install software-properties-common
sudo add-apt-repository universe
```
Ahora configuraremos nuestro sistema para que este reciba automaticamente actualizaciones de ros2 cuando las hayan

```bash
sudo apt update && sudo apt install curl -y
export ROS_APT_SOURCE_VERSION=$(curl -s https://api.github.com/repos/ros-infrastructure/ros-apt-source/releases/latest | grep -F "tag_name" | awk -F\" '{print $4}')
curl -L -o /tmp/ros2-apt-source.deb "https://github.com/ros-infrastructure/ros-apt-source/releases/download/${ROS_APT_SOURCE_VERSION}/ros2-apt-source_${ROS_APT_SOURCE_VERSION}.$(. /etc/os-release && echo ${UBUNTU_CODENAME:-${VERSION_CODENAME}})_all.deb"
sudo dpkg -i /tmp/ros2-apt-source.deb
```
Ahora para el futuro donde nosotros queremos crear herramientas de desarrollo es importante instalar sus herramientas propias

```bash
sudo apt update && sudo apt install ros-dev-tools
```

# Paso 2

Ahora si podemos proceder con la instalación de ros una vez que tenemos nuestro equipo configurado

```bash
sudo apt update
sudo apt upgrade
sudo apt install ros-jazzy-desktop
```

