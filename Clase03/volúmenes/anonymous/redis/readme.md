# Redis - Volumen anónimo

### Crear un contenedor de redis con un volumen anónimo

```
docker run -d --name server-redis01 -v /data redis:alpine
```

### Crear un contenedor cliente de Redis

```
docker run -d --name client-redis -p 8081:8081 -e REDIS_HOST=172.17.0.2 rediscommander/redis-commander:latest
```
