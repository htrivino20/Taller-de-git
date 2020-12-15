# Taller de Git y Github


## Objetivo del taller
El taller tiene como objetivo introducir conceptos básicos relacionado al software de control de versiones Git, conocer el flujo de trabajo de un proyecto relacionando la creación de ramas, solución de conflictos y llevar un repositorio local a un repositorio remoto para el trabajo colaborativo.

## Requerimientos 
### Instalación
Visitar: [Download Git](https://git-scm.com/downloads)
Turorial recomendado: [Tutorial](https://myhanoli.com/2018/08/25/5-pasos-para-instalar-git-en-windows/)

### Cuenta en github
Visitar: [Github](https://github.com/)

## Comandos
En las tablas posteriors, se presentan los comandos más comunes empleados en la terminal.

### Comandos Bash
|Comandos|Descripción|
|--|--|
|`pwd`|Muestra la ruta del directorio actual|
|`mkdir`|Crea un nuevo directorio|
|`ls`|Lista los archivos y directorios|
|`ls -a`|Lista todos los documentos incluso los ocultos|
|`ls -l`|Lista los documentos con fecha|
|`ls -al`|Lista todos los documentos incluso los ocultos con fecha|
|`cd <nombre del directorio>`|Permite movernos entre directorios|
|`touch <nombre del archivo>`|Crea un archivo con el nombre y extensión indicado|
|`clear`|Borra las líneas escritas en la terminal|
|`history`|Muestra todos los comandos escritos por el usuario.|

### Comandos Git
|Comandos|Descripción|
|--|--|
|`git help`|Muestra la lista de comandos más utilizados en Git|
|`git init`|Crea localmente un repositorio en Git|
|`git status`|Indica el estado del repositorio, por ejemplo, las modificaciones|
|`git add <nombre del archivo>`|Agrega al repositorio el archivo seleccionado|
|`git add .`|Agrega al repositorio el directorio seleccionado|
|`git commit -m "mensaje"`|Realiza un commit de las modificaciones|
|`git log`|Muestra el historial de commits con su descripción|
|`git branch`|Muestra la lista de ramas que existen en el repositorio|
|`git branch <nombre de rama>`|Crea una rama con el nombre indicado|
|`git checkout <nombre de rama>`|Permite moverse entre ramas	|
|`git merge <nombre de rama>`|Combina los cambios entre dos ramas|
|`git remote add origin [URL]`|Lleva un repositorio local a un repositorio remoto|
|`git pull origin main --allow-unrelated-histories`|Lleva los cambios realizados en el repositorio remoto al repositorio local permitiendo historias no relacionadas|
|`git push origin main`|Lleva los cambios del repositorio local, al repositorio remoto|

## Inicializar un repositorio local para llevarlo a Github
Para inicializar un nuevo repositorio, debemos dirigirnos en la carpeta donde ubicaremos el proyecto, luego:

 1. **Click derecho**, 
 2. Seleccionamos **Git Bash Here**, 
 3. Inicializamos el repositorio con comando `git init`.Al ejecutar el comando se creará un directorio `.git`, que se puede visualizar al activar la vista de archivos ocultos.
4.  Para realizar el primer commit, se deben agregar los nuevos archivos al staging area con `git add <nombre del archivo>` para un archivo en particular, o `git add .` para agregar todos los archivos del directorio.
5. Para realizar el commit se ejectua `git commit -m "mensaje"`; es una buena práctica dejar un mensaje relacionado a los cambios realizados.
6. Se ejectua `git status` para visualizar el estado del repositorio, si nos encontramos en la rama master creamos una nueva rama con el nombre main `git branch main`, Github está en proceso de cambio de nombre de la rama `master` a `main`.
7. Se crea un nuevo repositorio remoto en Github.
8. Para llevar el repositorio local a Github, se ejecuta `git remote add origin [URL]`, la URL se obtiene desde Github.
9. Se realiza un pull para obtener los archivos dentro del repositorio `git pull origin main --allow-unrelated-histories` la bandera debido a que ambos repositorios tienen distintas historias.
10. Finalmente, `git push origin main` lleva todos los cambios al repositorio remoto.

