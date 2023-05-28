# Indica la imagen base sobre la que se basara esta imagen
FROM nginx:1.23.2

# Borra la pagina por default de NGINX
RUN rm /etc/nginx/conf.d/default.conf

# Copia la carpeta de nuestro contexto al del contenedor y la configuracion de nuestro NGINX
COPY public /usr/share/nginx/html
COPY web.conf /etc/nginx/conf.d/web.conf

# Exponer el puerto 80
EXPOSE 80

# Iniciar el servicio de NGINX
CMD ["/usr/sbin/nginx", "-g", "daemon off;"]
