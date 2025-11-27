 # No todo es color rosa

En caso de que te equivocaste o te diste cuenta que tu versión de linux o cualquier otro motivo necesitas desinstalar ros estos son los comandos:

```bash
sudo apt remove ~nros-jazzy-* && sudo apt autoremove
```
Y despues actualizamos:

```bash
sudo apt remove ros2-apt-source
sudo apt update
sudo apt autoremove
sudo apt upgrade
```
