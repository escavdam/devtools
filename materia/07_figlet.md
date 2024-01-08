# Figlet

Figlet es una herramienta para crear arte con texto ascii desde la terminal:

 @@@@@@@  @@@       @@@@@@@@   @@@@@@   @@@@@@@   @@@@@@@    @@@@@@   @@@@@@@   @@@@@@
@@@@@@@@  @@@       @@@@@@@@  @@@@@@@@  @@@@@@@@  @@@@@@@@  @@@@@@@@  @@@@@@@  @@@@@@@@
!@@       @@!       @@!       @@!  @@@  @@!  @@@  @@!  @@@  @@!  @@@    @@!    @@!  @@@
!@!       !@!       !@!       !@!  @!@  !@!  @!@  !@!  @!@  !@!  @!@    !@!    !@!  @!@
!@!       @!!       @!!!:!    @!@!@!@!  @!@!!@!   @!@  !@!  @!@!@!@!    @!!    @!@!@!@!
!!!       !!!       !!!!!:    !!!@!!!!  !!@!@!    !@!  !!!  !!!@!!!!    !!!    !!!@!!!!
:!!       !!:       !!:       !!:  !!!  !!: :!!   !!:  !!!  !!:  !!!    !!:    !!:  !!!
:!:        :!:      :!:       :!:  !:!  :!:  !:!  :!:  !:!  :!:  !:!    :!:    :!:  !:!
 ::: :::   :: ::::   :: ::::  ::   :::  ::   :::   :::: ::  ::   :::     ::    ::   :::
 :: :: :  : :: : :  : :: ::    :   : :   :   : :  :: :  :    :   : :     :      :   : :

## Instalación

En linux/OSX podemos instalarlo con:

```bash
$ sudo apt-get install figlet
```

En windows podemos instalarlo descargando desde [aquí](http://www.figlet.org/).

## Uso

1. Comprueba que está instalado en la terminal:

```bash
$ figlet "Hola Mundo"
```

Podemos usar fuentes diferentes:

```bash
$ figlet -f slant "Hola Mundo"
```
Podemos ver las fuentes instaladas con:
    
```bash
figlet -f -l
```

Puedes descargar muchas fuentes adicionales desde [aquí](http://www.figlet.org/fontdb.cgi), también hay repositorios en github con fuentes adicionales ;)

# Práctica

1. Instálalo, comprueba que figlet funciona y puedes acceder a las fuentes instaladas.
2. Situate donde prefieras con la terminal, por ejemplo, en el escritorio.

```bash	
cd Desktop
```

3. Crea un directorio llamado `practica_figlet` y accede a él.

```bash
mkdir practica_figlet
cd practica_figlet
```

4. Crea un fichero llamado `hola_mundo.txt`.

```bash
echo practica.txt
```

5. Escribe en el fichero `hola_mundo.txt` el resultado de un comando figlet con el texto que prefieras.

```bash
figlet "Hola Mundo" > hola_mundo.txt
```

6. Crea un fichero llamado `practica.txt` y escribe en él el resultado de un comando figlet con el texto que prefieras y **una fuente que no sea la que viene por defecto.**