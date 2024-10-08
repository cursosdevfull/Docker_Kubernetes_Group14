# Redes

### Crear una red de tipo bridge

```
docker network create <nombre de la red> -d bridge
```

### Listar redes

```
docker network ls
```

### Crear contenedor vinculado a una red

```
docker run -d --network <nombre o id de la red> <nombre o id de la imagen>:<versión o tag>
```

### Inspeccionar una red

```
docker network inspect <nombre o ip de la red>
```

### Conectar un contenedor a una red

```
docker network connect <nombre o id de la red> <nombre o id del contenedor>
```

### Desconectar un contenedor a una red

```
docker network disconnect <nombre o id de la red> <nombre o id del contenedor>
```

### Crear un contenedor asociado a una red host

```
docker run -d --network host prom/prometheus
```
