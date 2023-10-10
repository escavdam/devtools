# Configuracion

Una vez instales Git, debes configurar tu nombre de usuario y tu correo electrónico. Esto es importante porque los commits de Git usan esta información, y es introducida de manera inmutable en los commits que envías:

```bash
git config --global user.name "Tu nombre"
git config --global user.email "tu correo"
```

Si quieres comprobar tus ajustes, puedes usar:

```bash
git config --list
```

Ya estás listo para empezar a trabajar con Git!

# Workflow

Lo primero que debemos hacer es inicializar un repositorio en el directorio donde se encuentra el código fuente del proyecto.
Nos movemos usando cd al directorio donde queremos crear nuestro proyecto y ejecutamos:
```bash
mkdir mi_proyecto # crea un directorio llamado mi_proyecto
cd mi_proyecto # nos movemos al directorio mi_proyecto
git init # inicializa un repositorio en el directorio actual
```

Una vez inicializado el repositorio, git comprobará si hay algún archivo en el directorio actual que no esté en el repositorio o si estos han sido modificados. Si es así, los podemos añadir al repositorio usando `git add .` para añadir todos los archivos modificados al área de preparación, y `git commit -m "Mensaje del commit"` para guardar los cambios en el repositorio.

```bash
git add . # añade todos los archivos modificados al área de preparación
git commit -m "Mensaje del commit" # guarda los cambios en el repositorio
```

Tambien podemos pasar el nombre del archivo que queremos añadir al área de preparación:

```bash
git add index.html # añade el archivo index.html al área de preparación
git commit -m "Creamos index.html" # guarda los cambios en el repositorio
```

Si ademas estas trabajando en un repositorio remoto, puedes sincronizar los cambios ejecutando `git push` para enviar los cambios al repositorio remoto.

```bash
git push # envia los cambios al repositorio remoto
```

Si vas a un pc donde no tengas tu repositorio, puedes descargar el repositorio usando `git clone`:

```bash
git clone url_de_github
```

Ya tenias el repositorio descargado, pero esta desactualizado? Puedes descargar los cambios del repositorio remoto usando `git pull`:

```bash
git pull # descarga los cambios del repositorio remoto
```

Esto es genial si trabajas en varios pcs, o si trabajas en un equipo con mas personas.

**Recuerda**
>Los mensajes de commit deben ser descriptivos y concisos. Deben explicar qué cambios se han realizado en el commit.

>Puedes añadir y agrupar los ficheros que quieras dentro de un mismo commit. Por ejemplo, si has modificado varios ficheros, puedes añadirlos todos al área de preparación y hacer un único commit con todos los cambios.

>No hagas commits sin mensaje.


