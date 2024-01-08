# FFMPEG

FFMPEG es una herramienta de línea de comandos que nos permite manipular archivos de video e imágenes. Es una herramienta muy poderosa y con muchas opciones, aunque solo saber algunos comandos os puede ser de mucha utilidad.

¿Alguna vez usaste algun editor de video? ¿Algun conversor online? ¿Alguna vez te preguntaste como plataformas como Twitch o YouTube pueden retransmitir datos de video de manera eficaz a tantos usuario? Estas plataformas usan FFMPEG (o una version modificada por ellos) para realizar estas tareas.

## Instalación

Para instalar FFMPEG en Ubuntu, ejecutamos el siguiente comando:

```bash
sudo apt install ffmpeg
```

Para instalarlo en Windows, podemos descargarlo desde la [página oficial](https://ffmpeg.org/download.html).

## Comandos

### Version

Para comprobar que se ha instalado correctamente, podemos ejecutar el siguiente comando:

```bash
ffmpeg -version
```

### Convertir un video

Para convertir un video de un formato a otro, podemos ejecutar el siguiente comando:

Puedes cambiar "input.mp4" por el nombre del archivo que quieras convertir y "output.avi" por el nombre y formato que desees

```bash
ffmpeg -i input.mp4 output.avi
```

### Comprimir un video

Para comprimir un video, podemos ejecutar el siguiente comando cambiando "video_in.webm" por el nombre del archivo que quieras comprimir y "archivo_comprimido.mp4" por el nombre y formato que desees

```bash
ffmpeg -i video_in.webm -vf "scale=iw*1.0:ih*1.0" -c:v libx264 -crf 23 -preset medium -c:a aac -b:a 128k archivo_comprimido.mp4
```

### Extraer un frame de un video

Para extraer un frame de un video, podemos ejecutar el siguiente comando:

```bash
ffmpeg -i video.mp4 -ss 00:00:01 -vframes 1 frame.png
```

Puedes variar el tiempo en el que tomas el frame cambiando el valor de "-ss 00:00:01" por el tiempo que desees.

### Cortar video

Necesitas acortar o quedarte con un trozo de un video?
En este caso, puedes editar tanto el tiempo de inicio como el tiempo de finalización del video, cambiando los valores de "-ss 00:00:05" y "-t 00:00:38" respectivamente.

```bash
ffmpeg -i video.mp4 -ss 00:00:05 -t 00:00:38 -c:v copy -c:a copy vídeo_cortado.mp4
```

### Extraer audio de un video

Para extraer el audio de un video, podemos ejecutar el siguiente comando:

```bash
ffmpeg -i video.mp4 -vn -acodec copy audio.mp3
```

### Automatas Celulares

FFMPEG incluye modelos de automatas celulares, que podemos ejecutar con el siguiente comando y modificando los valores de "rule" y "s":

```bash
ffplay -f lavfi -i cellauto=p="@":rule=30:s=600x600:full=0:scroll=0
```

### Glitch

Estos automatas celulares pueden ser usados para crear efectos glitch en videos:

```bash
ffmpeg -f lavfi -i cellauto=s=640x360:rule=15:r=50 -vf "scale=1280x720,format=yuv420p" -bsf noise=1000 -r 30 -f mpegts -c:v libx264 -crf 31 -preset ultrafast -tune zerolatency - | ffplay -i - -loglevel quiet -fs -vf tblend=all_mode=darken
```

> Por Rob Mac's submission para el Blue \x80 glitch art show de París
