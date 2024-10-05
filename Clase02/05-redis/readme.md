# Redis

### Crear contenedor sin password

```
docker run -d --name server-redis01 -p 6380:6379 redis:alpine
```

### Crear un contenedor con password

```
docker run -d --name server-redis02 -p 6381:6379 redis:alpine redis-server --requirepass todovale
```

### Crear un cliente de redis

```
docker run -d --name client-redis -p 8081:8081 -e REDIS_HOST=172.17.0.10 -e REDIS_PASSWORD=todovale rediscommander/redis-commander:latest
```
