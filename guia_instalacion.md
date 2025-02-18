## Añadir la Clave GPG: 
Utiliza el siguiente comando para añadir la clave GPG de Plex:
```
curl https://downloads.plex.tv/plex-keys/PlexSign.key | gpg --dearmor | sudo tee /usr/share/keyrings/plexserver.gpg > /dev/null
```
## Añadir el Repositorio:
Luego, utiliza el siguiente comando para añadir el repositorio de Plex:
```
echo deb [arch=amd64 signed-by=/usr/share/keyrings/plexserver.gpg] https://downloads.plex.tv/repo/deb public main | sudo tee /etc/apt/sources.list.d/plexmediaserver.list
```
## Actualizar el Sistema:
Ejecuta un actualización del sistema para que reconozca el nuevo repositorio:
```
sudo apt update
```
## Comando para Instalar Plex en Ubuntu 22.04 Server
Una vez que tenemos todo preparado, instalar el servidor Plex es muy sencillo utilizando el gestor de paquetes APT. Aquí te muestro el comando:
```
sudo apt install plexmediaserver
```
## Verificar la Instalación
Asegúrate de que Plex se está ejecutando:
```
systemctl status plexmediaserver
```
