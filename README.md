# SISTEMAS INFORMATICOS: INSTALACIÓN Y CONFIGURACIÓN DEL SERVIDOR NGINX, VIRTUAL HOSTS.

En esta actividad se pretende desplegar dos dominios de https://onehtmlpagechallenge.com/ en dos subdominios distintos usando NGINX

## 1 Instalación de una maquina vitual UBUNTU

Debido a las difiultades de instalar este servidor web/proxy en windows, debemos descargarnos una distribución linux y realizar el trabajo desde ahi.

<img src="https://i.gyazo.com/ba2fc16823f01ea2a698ee772dac5114.png">

## 2 Configuracion de la maquina UBUNTU

Usando el comando sudo apt update actualizamos las aplicaciones del sistema operativo.

<img src="https://i.gyazo.com/a5d58ea39ff5a565b146d12c32bebfde.png">

## 3 Instalamos NGINX

Con el comando sudo apt-get install nginx instalamos el servidor nginx en nuestro sistema operativo

<img src="https://i.gyazo.com/f52cc6ccd92a5705a57ff062d3450b7d.png">
Introducimos la letra "Y" para confirmar y continua nuestra instalación
<img src="https://i.gyazo.com/0f7596f94606c0c860e6d25feeceb328.png">

## 4 Localhost

Nos vamos a nuestro navegador de internet y en el buscador introducimos localhost donde nos saldrá un mensaje de NGINX como el que se muestra a continuación.

<img src="https://i.gyazo.com/a181ce45fe6ac832bbc1a7eb866daa4e.png">

## 5 Directorio de configuracion

Siguiendo la ruta /etc/nginx observamos el directorio de nginx

<img src="https://i.gyazo.com/34ce14b9e621c3c9bdb3e1bc65f03d62.png">

Aqui hay dos sitios que nos interesan, son sites-available y sites-enabled, en el sites-available guardaremos loas sitios disponibles, y en sites-enabled guardaremos los sitios activados

Como configuracion preestablecida en sites-available se encuentra el archivo de configuracion del servidor llamado default, y en sites enabled hay un enlace que apunta a el archivo default.

<img src="https://i.gyazo.com/a2dbb2f6fdee91441edfa0e26f5eeafc.png">
<img src="https://i.gyazo.com/163d83394c515d4c9d4f6c1778bd4a4c.png">

## 6 Configurar default

Haciendo dos copias del archivo default, donde configuraremos el archivo.

<img src="https://i.gyazo.com/f2a0cb91d1103f690288b9a406aa6b1e.png">

Asi esta configurado el archivo default.

<img src="https://i.gyazo.com/3799781da862ff3395e6c02ce38e084b.png">

Asi deberiamos dejarlo para que funcione.
<img src="https://i.gyazo.com/ec03b0abd2353ca5bdc35e290ddeebab.png">

Tambien cambiamos el root y el server name.
<img src="https://i.gyazo.com/3f7d4e77e24df37706a7607816d34496.png">

Hacemos lo mismo para configurar la segunda página.
<img src="https://i.gyazo.com/95548a7ca1c1a7364535160056bac6d8.png">

## Eleccion de las páginas web

Buscando la finalidad de esta actividad, subiremos dos páginas web al servidor en dos subdominios distintos, para ello cogeremos dos html de https://onehtmlpagechallenge.com/, en mi caso serán ASCII CAM y ADJUSTABLE FIREWORKS.

Dentro de www/pruebas crearemos lo siguiente

Creamos el archivo index.html que contendrá el código de la página 1
<img src="https://i.gyazo.com/a5e0e78dfc8a3720122ac1ffe4adf39b.png">

Creamos el archivo index.html que contendrá el código de la página 2
<img src="https://i.gyazo.com/409a2df7f2ad0c865f628341255a09d6.png">

## Configuracion del archivo hosts

Una vez hecho configuraremos los hosts para que los archivos se enlacen con el servidor para lo cual copiaremos la IP del servidor local y pondremos el nombre al que debe de ir a buscar
<img src="https://i.gyazo.com/665bbb7b11d2055875a4b4e9f0d14028.png">

## Comprobacion de resultados

Una vez todo configurado, reiniciamos el servidor NGINX, 
<img src="https://i.gyazo.com/19484b3d2173b8d52349cf5d9f8cf27d.png">

Nos vamos a nuestro navegador favorito e introducimos las URL que hayamos creado.

Pagina 1
<img src="https://i.gyazo.com/cf0db341e54a08c62cb7f353a0059b9c.png">
Nota: para usar esta página se debe de dar acceso a la cámara de la maquina que estemos usando.

Pagina 2
<img src="https://i.gyazo.com/7051907f97e385bcecb6571dd1ced2b3.png">

Fin.