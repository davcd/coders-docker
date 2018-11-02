Presentación (Objetivos de la charla)
Sobre mi (Experiencia con Docker)
Repositorio


[Introduccion]
¿Que es una máquina virtual?
LXC y las Grandes compañias
¿Que es un contenedor? (Sistema de ficheros, espacio de usuarios y procesos, interfaz de red, VM Ligera...)
Maquinas Virtuales vs. Containers (Recursos (precio), Cantidad, Tiempo arranque, Seguridad,... )
Microservicios (Definición, evolución SOA, relacción microservicios-containers, no inversa,...)
Docker (2013, Solomon Hykes, Go, cgroups, namespaces, go)
Ligereza (Recursos, Cantidad, Único kernel)
Portabilidad (Imágenes)
Inmutabilidad ("En mi máquina funciona, similitud imagenes con repositorios git")
Docker Daemon, Docker Registro, Cliente Docker
Docker-Hub (Similitud con GitHub, Imagenes Oficiales, Tags, Readme, ...)


[Imágenes]
Imagen(sistema de ficheros con metadatos, se inicia vacio, docker build recibe un Dockerfile y un contexto, tambien se puede hacer from scratch)
Dockerfile (From: definir la imagen base, RUN, ejecutar un comando, CMD-ENTRYPOINT: comando-entrypoint al arrancar, WORKDIR: definir directorio de trabajo, ENV: definir variables de entorno, EXPOSE: exponer un puerto, VOLUME: definir volumenes, COPY-ADD:copiar ficheros dentro de una imagen)
Caché(docker pull de la imagen base o docker build --pull, docker build --no-cache)


[Contenedores]
docker-compose (otro proyecto opensource, agiliza docker run)
Volúmenes (Datos: persistencia, compartible, no son gestionados por los storage drivers, Host: montar carpetas del host)
Redes(compose crea redes bridge, Bridge: red principal, Redes Overlay: multi host, )


[Avanzado]
Gestion de clusteres (swarm: solucion de Docker, manda la sencillez. Kubernetes: desarrollado por google, es el mas popular. Go, release 2014. )


