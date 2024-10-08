# Redes compartidas

### Crear redes

```
docker network create net-curso14-1 -d bridge
docker network create net-curso14-2 -d bridge
```

### Crear contenedores

```
docker run -d --name server-nginx01 --network net-curso14-1 nginx:alpine
docker run -d --name server-nginx02 --network net-curso14-1 --network net-curso14-2 nginx:alpine
docker run -d --name server-nginx03 --network net-curso14-2 nginx:alpine
```
