# Rutas

Tanto en la terminal, como en html, css y javascript, las rutas son muy importantes, ya que nos permiten acceder a archivos y directorios.

Imagina un directorio con la siguiente estructura de archivos:

```bash
/portfolio_web
├── css
│   └── style.css
├── img
│   └── logo.png
└── index.html
```

## Rutas absolutas

Las rutas absolutas son aquellas que empiezan desde la raíz del sistema de archivos.

En el caso de la terminal, la ruta absoluta empieza desde la raíz del sistema de archivos.

```bash
$ pwd
/home/usuario
$ cd /home/usuario/portfolio_web
$ ls
css  img  index.html
```

En el caso de html y javascript, la ruta absoluta empieza desde la raíz del servidor web.

```html
<img src="/img/logo.png" alt="Logo">
```

## Rutas relativas

Las rutas relativas son aquellas que empiezan desde el directorio actual.

En el caso de la terminal, la ruta relativa empieza desde el directorio actual.

```bash
$ pwd
/home/usuario
$ ls
portfolio_web Documentos  Imágenes  Música  Plantillas  Público  Vídeos
$ cd portfolio_web
$ ls
css  img  index.html
```

En el caso de html y javascript, la ruta relativa empieza desde el directorio actual.

```html
<img src="img/logo.png" alt="Logo">
```

## Rutas relativas con `..`

El directorio `..` nos permite acceder al directorio padre, es decir, al directorio que contiene al directorio actual.

En el caso de la terminal, podemos usar `cd ..` para acceder al directorio padre.

```bash
$ pwd
/home/usuario/portfolio_web/css
$ cd ..
$ pwd
/home/usuario/portfolio_web
```

En el caso de html, css y javascript, podemos usar `../` para acceder al directorio padre.

```html
<img src="../img/logo.png" alt="Logo">
```

## Rutas relativas con `.`
El directorio `.` nos permite acceder al directorio actual.

En el caso de la terminal, podemos usarlo para especificar una ruta desde donde nos encontramos actualmente.

```bash
$ pwd
/home/usuario/portfolio_web
$ ls
css  img  index.html
$ ls ./css
style.css
```

De la misma manera en html, css y javascript, podemos usar `./` para especificar una ruta desde donde se encuentra el fichero donde estamos escribiendo.

```html
<img src="./img/logo.png" alt="Logo">
```


