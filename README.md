# Docker Workshop

Teniendo en cuenta la documentación de Docker, cree un archivo Dockerfile que construya una imagen para ejecutar la aplicación en Node que está en este repositorio. Los requerimientos son:

- La imagen debe extender de node versión 16.13.2-slim.
- La imagen debe exponer el puerto 3020, el cual es el puerto que usa la aplicación.
- La imagen debe copiar el archivo package.json dentro de ella.
- La imagen debe copiar el archivo app.js dentro de ella.
- La imagen debe instalar (en fase de build) todos los paquetes necesarios por medio del comando npm install.
- La imagen debe ejecutar el comando node app.js en fase de runtime. Esta ejecución debe ser tipo exec y no tipo shell. Para mayor información revise la documentación de docker.

Para lograr el objetivo tenga en cuenta los siguientes pasos:

### Primero) Cree el archivo dockerfile

- Descargue este repositorio en su máquina local.
- Cree el archivo Dockerfile al mismo nivel que el archivo app.js.
- Configure el archivo para que cumpla con los requerimientos especificados anteriormente.

### Segundo) Cree la imagen localmente

- Abra un terminal y ubíquese en la ruta del proyecto (al mismo nivel de los archivos app.js y Dockerfile).
- Use el comando de construcción de imágenes de docker haciendo uso del tag "hello-node". Recuerde que por estar ubicado en el mismo sitio del Dockerfile la ruta para el archivo es únicamente un punto ( . ).
- Valide que se haya creado la imagen correctamente por medio del comando que lista las imágenes de docker.

### Tercero) Ejecute el contenedor

- Ejecute el comando que ejecuta la imagen "hello-node" en su máquina. Recuerde que debe hacer un mapeo de puertos para que pueda acceder al servicio en su máquina física.
- Valide por medio de su navegador el funcionamiento de la aplicación, accediendo a la ruta "http://localhost:puerto/hello"

### Cuarto) Publicación en un registry

Con la aplicación en funcionamiento, solo queda publicarla en un registro. Para ello haga uso del registro de Github siguiendo los pasos en esta [guía](https://docs.github.com/en/packages/working-with-a-github-packages-registry/working-with-the-container-registry)

Éxitos!!
