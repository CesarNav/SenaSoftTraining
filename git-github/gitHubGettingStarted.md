# Git y Github

## Git

Git es un sistema de control de versiones (SCV) esencial en el desarrollo de proyectos de tecnologia pues nos permite tener un flujo de trabajo trasparente y confiable. Git nos permite terner un registro de los cambios hechos en el proyecto e identificar que miembro del equipo lo realizó.

## GitHub

Para usar git es necesario contar con un servicio que nos permita almacenar nuestro repositorio de manera remota, entre los más populares se encuentra Github y Gitlab.

## Descargar Git

- Lo primero que debemos hacer es descargar Git en caso de que nuestra maquina no lo tenga.

```
https://git-scm.com/downloads
```
- Seleccionamos nuestro sistema operativo y automaticmanete iniciará la descarga.

- Ejecutamos el archivo y seguimos los pasos del asistente.

## Iniciar en GitHub

Para iniciar se debe crear una cuenta en github, en caso de no poseer una.

- En el navegador vamos a la siguiente url
``` 
https://github.com/
```
- Se ingresa a la seccion de "Sign up" y se llena el formulario.

- Luego de  terminar el proceso de registro se verifica el correo y se ingresa.

## Crear un repositorio

Un repositorio es el lugar donde vamos a guardar todos los cambios de nuestro proyecto.

- En la esquina superior izquierda, bajo nuestra foto de perfil existe un botón verde que dice "New", le damos click para crear un nuevo repositorio.

- Asignamos un nombre, una descripción, si deseamos, y elegimos si será un repositorio público o privado.

- Podemos elegir iniciar el repositorio con una licencia según la naturaleza de nuestro proyecto o un read.me, que es la descripción del proyecto.

- Terminamos de crear el repositorio dando clic en "Create repository"

## Configuracion incial

Debemos configurar nuestro usuario para que Git pueda identificar quien hace los cambios.

- Lo primero que hacemos es abrir la consola del Git bash, lo podemos hacer buscando en el menú de inicio.
```
"bash" 
```
- Así mismo podemos acceder a ella dando clic derecho dentro de la carpeta donde queremos tener el repositorio y seleccionando la opción.
```
Git bash here

```
- Una vez en la terminal configuraremos nuestro nombre y correo de usuario
```
git config --global user.name 'nombre'
```
```
git config --global user.email 'correo@electronico'
```
## Clonar un reopositorio

Existen dos repositorios, el local que está en nuestra maquina y el remoto que es el de GitHub

Para tener en nuestra maquina el repositorio de Github hayq ue clonarlo.

- Damos clic la pestaña "<>code" de nuestro repositorio en GitHub

- Damos clic en el botón verde con la palabra "code" y copiamos el link que allí aparece

- En nuestro terminal local escribimos el comando git clone y el link del repositorio
```
git clone https://github.com/CesarNav/SenaSoftTraining.git
```
Una vez hecho esto Git va a descargar todos los archivos del repositorio remoto de GitHub, en nuestro repositorio local, junto con una carpeta oculta llamada ".git", que es la configuración del repositorio.

## Comandos

- Para verificar el estado de nuestro repositorio y los cambios pendientes ejecutamos
```
git status
```
- Para añadir un archivo nuevo, necesitamos que git empiece a identificarlo (Traking), para esto ejecutamos git add y el nombre del archivo que deseamos git identifique, si son muchos archivos podemos poner un punto "." , esto indica que todo loq ue hay en ese directorio sera identificado.
```
git add .
```

- Git puede estar indentificando los cambios o archivos nuevos, pero no significa que los haga parte del repositrio. Para comprometer el archivo, es decir que se envie al repositorio como un punto en el timepo, se ejecuta el comando git commit -m y un mensaje para descirbir el commit, entre comillas.
```
git commit -a "Este es un commit"
```

- Una vez hemos comprometido los archivos nuevos en nuestro repositorio local, debemos enviarlos al repositorio remoto, para esto se jecuta el comando git push.
```
git push
```
- Para trar archivos del repositorio remoto, que no esten en el local, debemos ejecutar le comando git pull. Esto traera todos los cambios que esten en el repositorio remoto, que no esten en nuestro repositorio local.
```
git pull
```

## Revisar nuestro repositorio

- Para visualizar los cambios realizados a traves del tiempo, debemos ejecutar el comando git log, esto nos traerá todos los commits que se hayan hecho en esta rama, el autor del commit, la fecha y el mensaje.
```
git log
```
- Con git tenemos la capacidad de volver a un punto en el tiempo, a un commit anterior y revisar que se habia hecho hasta entonces, para esto se ejecuta el comando git checkout y los 6 primeros digitos del commit. Para volver al presente se coloca main, en lugar de los digitos.
```
git checkout ab3b72
```
## Branches o Ramas
- En git una rama es una derivacion del flujo de trabajo que permite desarrollar ciertas actividades sin que estas intervengan con el flujo de otras. Por lo general se usan tres ramas, la rama de desarrollo, la rama de testing y la rama principal.

- Para verificar en que rama se está trabajando actualmente se ejecuta el comando git branch 
```
git branch
```
- Para ver todas las ramas del repostorio se ejecuta
```
git branch -a
```
- Para crear una nueva rama se ejecuta el codigo git checkout -b y el nombre de la nueva rama.
```
git checkout -b developer
```
- Para cambiar te rama se ejecuta el git chockout pero con el nombre de la rama
```
git checkout developer
```
## Merge
El merge es un comando que nos permite mezclar dos ramas y conservar los cambios de mabs en una sola
- Para hacer un merge nos situamos en la rama que queremos mezclar y ejecutamos el comando git merge con el nombre de la rama con la cual la vamos a mezclar
```
git merge main
```

## Fork
GitHub es una comunidad donde la gente colabora en repositorios de codigo abierto (Open Source) es decir que le codigo puede ser copiado y descargado por cualquier persona y realizar sus porpias modificaciónes sin afectar el original.

Un Fork es como copiamos y descargamos ese codigo desde GitHUb para tener una copia persona de todo el repositorio.

- En la esquina superior derecha del repositorio existen tres botones, "Watch" para seguir el repositorio, "Star" es una especie de favorito y "Fork", que es copiarlo.

- damos clic en Fork y una vez completado el proceso aparecerá como un repositorio ligado a nuetsra cuenta de github, se clona en el local y se trabaja de maner anormal como otro repositorio.

## Pull request
Un pull request nos permite pedir que se haga un merge en una rama o repositorio con una contribución nuestra, cuanod no somos los editores del repositorio.