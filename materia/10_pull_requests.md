# Pull requests

Un pull request es una petición que se hace a un repositorio en github para que se incorporen los cambios que se han hecho en un fork de ese repositorio.

Los pasos para hacer un pull request son los siguientes:

1. Hacer un fork del repositorio en el que queremos trabajar.
2. Clonar el repositorio en nuestro ordenador.
3. Crear una rama en nuestro repositorio local.
4. Hacer los cambios que queramos en esa rama.
5. Hacer un commit de los cambios que hemos hecho.
6. Hacer push de los cambios que hemos hecho.
7. Hacer un pull request en github.

## Hacer un fork

Para hacer un fork de un repositorio, vamos a la página del repositorio en github y hacemos click en el botón `Fork`.

![fork](fork.png)

Esto creará una copia del repositorio en nuestra cuenta de github, completamente aparte del repositorio original.

## Clonar el repositorio

Ya sabeis hacer esto, pero por si acaso:

```bash
git clone <url_del_repositorio>
```

## Crear una rama

Para crear una rama, ejecutamos `git branch <nombre_rama>` en la terminal o utilizamos las herramientas que nos ofrece nuestro editor de código.

![branch](/imgs/branch.png)

![branch2](/imgs/branch1.png)

## Hacer cambios

**ASEGURATE** de que estás en la rama correcta antes de hacer cambios con `git checkout <nombre_rama>`.

Haz los cambios que quieras en el código.

## commit y push

Realiza tu commit como de costumbre, luego haz push de la rama que has creado a tu repositorio remoto.

## Hacer un pull request

Vuelve a tu repositorio en github, deberias poder ver la rama que has creado y un botón para hacer un pull request al repositorio de origen.