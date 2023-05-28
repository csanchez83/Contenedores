# Ejemplo, sitio estatico con NGINX


# Construir imagen en base a nuestro DockerFile
    sudo docker build -t app:v1 .
    
- "build" es la directriz para construir la imagen
- "-t" crearle un tag
- "." buscara localmente un archivo llamado Dockerfile


# Correr nuestro contenedor
    sudo docker run -d -p 80:80 app:v1
    
# Datos de nuestros contenedores corriendo
    sudo docker ps
    
# Datos de nuestros contenedores en general
    sudo docker ps -a
    
# Imagenes que tenemos
    sudo docker images
    
# Logs
    sudo docker logs
    
    
