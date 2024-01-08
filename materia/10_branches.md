# Branches

Hasta ahora hemos trabajado en la rama `main` de nuestro repositorio. Esta rama es la creada por defecto cuando creamos un repositorio y la que se utiliza para publicar los cambios que se han hecho en el mismo.

Sin embargo, trabajar en la rama `main` no es una buena práctica, git nos ofrece una forma de crear y añadir nuevas funcionalidades a nuestro código de una forma más segura: las ramas.

## Crear una rama

Para crear una rama, ejecutamos `git branch <nombre_rama>` en la terminal o utilizamos las herramientas que nos ofrece nuestro editor de código.

Para movernos a una rama, ejecutamos `git checkout <nombre_rama>` en la terminal o utilizamos las herramientas que nos ofrece nuestro editor de código.

## Que es una rama

Una rama es una copia del código de nuetro repositorio en el momento en que se crea la rama. A partir de ese momento, podemos hacer cambios en la rama sin afectar al código de la rama `main`.

Podemos crear tantas ramas como queramos, y podemos movernos entre ellas utilizando `git checkout <nombre_rama>`.

Podemos usar `commit` en una rama para guardar los cambios que hemos hecho en esa rama y `push` para subir esos cambios a nuestro repositorio remoto.

## Merge

Una vez hemos terminado de trabajar en una rama, podemos incorporar los cambios que hemos hecho en esa rama a la rama `main` utilizando `git merge <nombre_rama>`, seguido de `git push` a nuestro repositorio remoto.

## Conflictos

Si hacemos cambios en la rama `main` y en otra rama, y después intentamos incorporar los cambios de la rama a la rama `main`, git nos avisará de que hay un conflicto entre los cambios que hemos hecho en la rama `main` y los cambios que hemos hecho en la otra rama.

**Recuerda** que github esta creado para trabajar de forma conjunta, puede que alguien haya hecho cambios en el repositorio mientras tu estabas trabajando en tu rama. Los conflictos pueden asustar, pero en muchos casos son fáciles de resolver en equipo gracias a los pull requests.
