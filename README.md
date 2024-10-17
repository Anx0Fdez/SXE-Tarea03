# Tarea 03
### <u>*Actividad 1</u>:*
*Descargar imagen Apache 2.4*
```bash
sudo docker pull httpd:2.4
```
*Comprobar que la imagen se ha descargado correctamente.*
```bash
sudo docker images
```
### <u>*Actividad 2</u>:*
*Crea un contenedor con el nombre 'dam_web1'.*
```bash
sudo docker run -d --name dam_web1 httpd
```
