# Github
Github es una plataforma de desarrollo colaborativo para alojar proyectos utilizando el sistema de control de versiones Git.

- [Whisper](https://github.com/openai/whisper)
- [RAVE](https://github.com/acids-ircam/RAVE)
- [Blog](https://github.blog/2023-09-29-game-bytes/)
- [SICP](https://github.com/fedehc/SICP-ES/tree/master)

# Github CLI
Github CLI es una herramienta de línea de comandos para trabajar con Github.
No es obligatoria, pero si queremos trabajar con repositorios privados, es necesario autenticarse con Github CLI.

## Instalación
Para instalar Github CLI, podemos descargarlo desde la página oficial de Github CLI: https://cli.github.com/

Una vez instalado, podemos comprobar que se ha instalado correctamente ejecutando `gh --version` en la terminal.

## Autenticación

Para autenticarnos con Github CLI, ejecutamos `gh auth login` en la terminal.

Se nos pedirá que introduzcamos nuestras credenciales de Github, y que introduzcamos un código de autenticación que se nos habrá enviado por correo electrónico.

Una vez autenticados, podemos comprobar que se ha autenticado correctamente ejecutando `gh auth status` en la terminal.

# Crear un repositorio

Para crear un repositorio, ejecutamos `gh repo create` en la terminal.

Tambien podemos crearlo en la interfaz web de github.