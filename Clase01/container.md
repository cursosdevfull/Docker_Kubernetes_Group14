# Contenedor

### Crear

```
docker create <nombre o id de la imagen>:<version o tag>
docker create --name <nombre contenedor> <nombre o id de la imagen>:<version o tag>
```

### Listar contenedores ejecutándose

```
docker ps
```

### Listar contenedores ejecutándose o no

```
docker ps -a
```

### Iniciar

```
docker start <nombre o id del contenedor>
```

### Detener

```
docker stop <nombre o id del contenedor>
```

### Eliminar

```
docker rm  awesome_engelbart
docker rm -f awesome_engelbart
```

### Crear un contenedor usando run

```
docker run nginx:alpine
docker run -d nginx:alpine
```

### Crear un contenedor con nombre

```
docker run -d --name server-nginx nginx:alpine
```

### Crear un contenedor con mapeo de puertos

```
docker run -d --name server-nginx -p 3000:80 nginx:alpine
docker run -d --name server-nginx-2 -p 3001:80 nginx:alpine
docker run -dp 3002:80 --name server-nginx-3  nginx:alpine
```

### Inspeccionar un contenedor

```
docker inspect <nombre contenedor | id>
```
