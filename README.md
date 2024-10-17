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
sudo docker run -d --name dam_web1 httpd:2.4
```
### <u>*Actividad 3</u>:*
*Creamos una carpeta donde alojaremos nuestra página web.*
```bash
mkdir ~/mi_web
```

*Crear un archivo index.html con el siguiente contenido: HOLA MUNDO*
```bash
cd mi_web
echo "<html><body><h1>Hola Mundo</h1></body></html>" > index.html
```

*Borramos el contenedor 'dam_web1' y creamos uno nuevo con el volumen de la carpeta 'mi_web'*
*Depues copiamos el archivo index.html a la carpeta htdocs del contenedor.*
```bash
sudo docker rm -f dam_web1
sudo docker run -d --name dam_web1 -p 8000:80 -v ~/mi-web:/usr/local/apache2/htdocs httpd
```
### <u>*Actividad 4</u>:*
*Comprobar que la página web se ha creado correctamente.*
```bash
http://localhost:8000
```
