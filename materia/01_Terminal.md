# Terminal
La terminal es una interfaz de texto que nos permite interactuar con el sistema operativo mediante comandos, es una herramienta muy potente, ya que nos permite realizar tareas de forma más rápida y eficiente que con una interfaz gráfica.

> **Recuerda** que al instalar programas nuevos, debes reiniciar la terminal para que los cambios surtan efecto.

## Abrir la terminal
Para abrir la terminal en Windows, podemos utilizar el comando `cmd` o `powershell` en el menú de inicio.

Para abrir la terminal en Linux, podemos utilizar el atajo de teclado `Ctrl + Alt + T`.

Para abrir la terminal en MacOS, podemos utilizar el atajo de teclado `Cmd + Espacio` y escribir `terminal`.

## Comandos básicos
### pwd
El comando `pwd` nos muestra la ruta del directorio actual.

```bash
$ pwd
/home/usuario
```

### ls
El comando `ls` nos muestra el contenido del directorio actual.

```bash
$ ls
Documentos  Imágenes  Música  Plantillas  Público  Vídeos
```

### cd
El comando `cd` nos permite cambiar de directorio.

```bash
$ cd Documentos
$ pwd
/home/usuario/Documentos
```

### mkdir
El comando `mkdir` nos permite crear directorios.

```bash
$ mkdir directorio
$ ls
directorio
```

### touch
El comando `touch` nos permite crear archivos.

```bash
$ touch archivo.txt
$ touch index.html
$ ls
archivo.txt  index.html
```

### rm
El comando `rm` nos permite borrar archivos.

```bash
$ rm archivo.txt
$ ls
index.html
```

Para borrar carpetas con todo su contenido, podemos utilizar el parámetro `-r`.

```bash
$ rm -r directorio
```

### mv
El comando `mv` nos permite mover archivos.

```bash
$ mv index.html Documentos

```

## Alias y scripting
Podemos crear alias para nuestros comandos favoritos, o crear scripts para automatizar tareas.

Para crear un alias, debemos editar el archivo `.bashrc` o `.bash_profile` y añadir la siguiente línea:

```bash
alias borrar='rm -r'
```

Para crear un script, debemos crear un archivo con extensión `.sh` y añadir los comandos que queramos ejecutar.

```bash
echo "Iniciando script"
python script.py
echo "Script finalizado"
```

## Herramientas de terminal

### [FIGlet](http://www.figlet.org/)
FIGlet es una herramienta que nos permite crear texto en formato ASCII, podemos instalarla en Mac y Linux con el siguiente comando:

```bash
$ sudo apt-get install figlet
```

Para utilizarla, simplemente debemos escribir `figlet` seguido del texto que queramos convertir.

```bash
$ figlet Hola mundo
```

### [FFMPEG](https://ffmpeg.org/)
FFMPEG es una herramienta que nos permite convertir archivos multimedia, podemos instalarla en Mac y Linux con el siguiente comando:

```bash
$ sudo apt-get install ffmpeg
```

Para utilizarla, simplemente debemos escribir `ffmpeg` seguido de los parámetros que queramos utilizar.

```bash
$ ffmpeg -i video.mp4 video.avi
```

Comprimir video
```bash
$ ffmpeg -i video_in.webm -vf "scale=iw*1.0:ih*1.0" -c:v libx264 -crf 23 -preset medium -c:a aac -b:a 128k archivo_comprimido.mp4
```

Podemos, desde convertir a otro formato de video, como exportar los frames, cortar, comprimir, etc.

```bash
ffmpeg -f lavfi -i cellauto=s=640x360:rule=15:r=50 \
-vf scale=1280x720 -bsf noise=1000 -r 30 -f mpegts \
-c:v h264 -crf 31 -preset ultrafast -tune zerolatency - | \
ffplay -i - -loglevel quiet -fs -vf tblend=all_mode=darken
```
>codigo por Rob Mac's para el evento Blue \x80

### [ImageMagick](https://imagemagick.org/index.php)
ImageMagick es una herramienta que nos permite editar imágenes, podemos instalarla en Mac y Linux con el siguiente comando:

```bash
$ sudo apt-get install imagemagick
```

Para utilizarla, simplemente debemos escribir `convert` seguido de los parámetros que queramos utilizar.

```bash
$ convert imagen.jpg imagen.png
```

Podemos, desde convertir a otro formato de imagen, como redimensionar, recortar, añadir texto, etc.

```bash
$ convert imagen.jpg -resize 50% imagen.png
```

Es muy util para redimensionar, renombrar y comprimir imágenes de forma masiva.

```bash
$ mogrify -resize 50% -quality 50% -path ./output *.jpg
```

### [youtube-dl](https://ytdl-org.github.io/youtube-dl/index.html)
youtube-dl es una herramienta que nos permite descargar videos de YouTube, podemos instalarla en Mac y Linux con el siguiente comando:

```bash
$ sudo apt-get install youtube-dl
```

Para utilizarla, simplemente debemos escribir `youtube-dl` seguido de la URL del video que queramos descargar.

```bash
$ youtube-dl https://www.youtube.com/watch?v=dQw4w9WgXcQ
```

Funciona con muchos otros sitios web, como Vimeo, Facebook, Twitter, etc.

