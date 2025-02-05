# Objetivo

No espero que seáis capaces de solucionar esta practica con vuestros conocimientos actuales, pretendo que busquéis información de forma autónoma para resolver los ejercicios que se os plantean. Mucha suerte.


# Creación de un servidor RTMP

Para realizar un servidor RTMP vamos a utilizar [Nginx](https://nginx.org/en/), ([Mas info](https://es.wikipedia.org/wiki/Nginx))

¿Define que es el protocolo RTMP? ¿Y el RTP? ¿En que se parecen?

# Procedimiento

## Nginx

Primero instala y configura el servidor web Nginx y el paquete Nginx-RTMP

````
apt install nginx 
apt install libnginx-mod-rtmp -y
````

Para asegurar que todo esta correcto emplea el siguiente comando:

````
nginx -t
````

Intenta que el servidor escuche al puerto 1935.

## Enviar video al servidor

Descarga un video de youtube ([por si no se os ocurre nada](https://www.youtube.com/watch?v=yNeprtMyAAg)) y una vez descargado usa el comando ffmpeg para descargarlo en el servidor.

## En cliente

En el VLC haz click en Medios > Abrir transmisión de red y haz click en Reproducir.

## Monitorización

Configura el servidor para acceder a la pagina de monitorización en http://IP:8080/stat

Tendréis que usar el archivo de estadísticas en la siguiente dirección: `/usr/share/doc/libnginx-mod-rtmp/examples/stat.xsl`

Cuando termineis avisadme y os doy nota.