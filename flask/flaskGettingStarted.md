# Flask y MySQL 

## Flask
Flask es un framework de desarrollo web escrito en python que nos permite crear aplicaciones web, se denomina a sí mismo como un microframework buscando que su estructura inicial sea lo más simple posible, no depende de un sistema de autenticacion o un sistema de base de datos especifico, sino que a medida que crece el proyecto se pueden ir añadiendo más extensiones.

## Pip
Pip es el manejador de paquetes de python, este viene integrado con el lenguaje una vez se descarga, para validar que tenemos pip ejecutamos en la linea de comandos.
    ```
    pip --version
    ```

## Entornos virtuales
Un entorno virtual nos permite tener encapsulados todos los paquetes y librerías de un proyecto para evitar que los mismos interfieran con los que están instalados en el sistema de manera global.
- Para instalar un entorno virntual ejecutamos el comando.
    ```
    pip install virtualenv
    ```
- Para iniciar un entorno virtual, nos ubicamos en el directorio donde queremos iniciarlo y ejecutamos el comando.
    ```
    virtualenv nombreDelEntorno
    ```
- Debemos ubicarmos en el directorio "bin" dentro de nuestro entorno 
    ```
    cd nombreDelEntorno/bin/
    ```
- Para activar el entorno debemos hasta el directorio "Scripts", dentro del entorno virtual y activarlo
    ```
    cd nombreDelEntorno/Scripts

    # Desde CMD o powershell
    ./activate

    # Desde bash o linux
    source ./activate
    ```
## Instalar flask
- Para instalar flask debemos estar dentro del entorno virtual y ejecutar
    ```
    pip install flask
    ```
- Para ver las dependecias instaladas ejecutamos 
    ```
    pip freeze
    ```
- Creamos un nuevo archivo llamado "requirements.txt" donde ponemos todas las dependecias que necesita nuestor proyecto para ejecutarse, para instalarlo se ejecuta el comando
    ```
    touch requirements.txt

    pip install -r requirements.txt
    ```
- Podemos enviar las dependencias al archivo "requirements.txt" ejecutando el comando.
    ```
    pip freeze > requirements.txt
    ```

## Iniciar proyecto
- Para inciar el proyecto creamos un nuevo archivo llamado main.py
    ```
    touch main.py
    ```
- En el archivo "main.py" escribimos
    ```
    from flask import Flask
    ```
    Flask es la clase que nos permite crear instancias de flask

- Una vez importada la clase, debemos hacer una instanciación.
    ```
    app = Flask(_name_)
    ```