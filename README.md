# Instalacion-nginx-PHP

### Descripción

---

1. Realiza la configuración básica de nginx que ejecute scripts PHP creando una receta ansible. Utilizando como base la receta ansible que utilizaste para el [taller 4](https://fp.josedomingo.org/sri2223/3_http/files/ejercicio_proxy.zip), modifícala para añadir las siguientes funcionalidades:

      - Instalación de los servicios (cada servicio se instalará y configurará en un rol diferenciado).
        
      - Además de copiar un index.html en el DocumentRoot, copiará también un fichero info.php que muestre la información de la configuración de PHP.
        
      - Como hace la receta original, creará virtualhost que tengas definido en una lista. Estos virtual host estarán configurados para ejecutar PHP.
        
      - La receta debe poder desactivar los virtualhost que tengas definido en otra lista.

2. Configura sobre una máquina virtual, usando la receta de ansible, un servidor nginx + PHP con dos virtualhost:
        
      - www.pagina1.org, cuyo DocumetRoot estará en /srv/www/pagina1.
        
      - www.pagina2.org, cuyo DocumetRoot estará en /srv/www/pagina2.

Una vez que la receta haya configurado el servidor web con los dos Virtualhost, configura manualmente las siguientes características:
    
3. Cuando se acceda a www.pagina1.org se realizará una redirección a a la página www.pagina1.org/principal. En el directorio principal no se permite ver la lista de los ficheros, no se permite que se siga los enlaces simbólicos.
    
4. En la página www.pagina1.org/principal se debe mostrar una página web estática (utiliza alguna plantilla para que tenga hoja de estilo o la página estática que has generado en IAW).
    
5. Si accedes a la página www.pagina1.org/principal/documentos se visualizarán los documentos que hay en /srv/doc. Por lo tanto se permitirá el listado de fichero y el seguimiento de enlaces simbólicos.
    
6. Limita el acceso a la URL www.pagina1.org/secreto con autentificación básica.

### Entrega

---

1. Entrega la URL del repositorio GitHub donde has alojado la práctica.
    
2. Pantallazos para comprobar que se han creado los dos virtualhost después de ejecutar la receta ansible.
    
3. Comprobación de que al acceder a www.pagina1.org se produce una redirección. Pantallazo accediendo desde un navegador web.
    
4. Pantallazo accediendo a www.pagina1.org/principal/documentos (pon algunos ficheros para que se vea la lista).
    
5. Pantallazos de la autentificación básica.
    
6. Finalmente, configura la receta ansible para desactivar el virtualhost www.pagina2.org. Pasa de nuevo la receta y manda algún prueba de que se ha borrado dicho VirtualHost.
