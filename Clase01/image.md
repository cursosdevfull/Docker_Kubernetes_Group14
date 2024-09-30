# Imágenes

### Listar

```
docker images
```

### Filtrar

```
docker images | grep hello
```

### Inspeccionar

```
docker image inspect <nombre de la imagen | id>:<versión de la imagen>
```

### Descargar

```
docker pull <nombre imagen>:<versión o tag>
```

### Eliminar

```
docker rmi nginx:alpine
docker rmi -f nginx:alpine
```
