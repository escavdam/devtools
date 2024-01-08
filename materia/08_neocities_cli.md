# Neocities CLI

Hasta ahora, has interactuado con neocities a través de su interfaz web, pero también puedes hacerlo desde la terminal.

No necesitas salir de tu editor para actualizar tu web de neocities, pero si necesitas una terminal y la herramienta de línea de comandos de neocities.

## Instalación

En linux/OSX podemos instalarlo con:

```bash
$ sudo gem install neocities
```

En windows debemos instalar primero [ruby](https://rubyinstaller.org/), y luego ejecutar:

```bash
$ gem install neocities
```

## Uso

1. Comprueba que está instalado en la terminal:

```bash
$ neocities
```

2. Inicia sesion con tu usuario y contraseña:

```bash
$ neocities login
```

Deberás introducir tu usuario (el nombre de tu web) y tu contraseña.

3. Puedes subir cualquier archivo o directorio con:

```bash
$ neocities push archivo.html
```

4. Puedes ver el estado de tu web con:

```bash
$ neocities info
```

5. Puedes subir todos los archivos de tu directorio con:

```bash
$ neocities push .
```

6. Puedes borrar archivos con:

```bash
$ neocities delete archivo.html
```

> **Recuerda** situarte con la terminal en el directorio adecuado, abriendo la carpeta en vscode es más fácil no equivocarse, ya que vemos los archivos que hay en cada directorio.
> **Recuerda** que debes tener cuidado al hacer una subida de **todo** lo que hay en tu directorio.