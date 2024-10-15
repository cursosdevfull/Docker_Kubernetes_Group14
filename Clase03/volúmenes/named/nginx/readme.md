# NGINX - Volúmen de tipo Named (Nombrado)

### Crear volumen nombrado

```
docker volume create vol-nginx
```

### Crear el volúmen usando la ruta relativa (Git Bash)

```
docker run -d --name server-nginx -p 9000:80 -v vol-nginx:/usr/share/nginx/html nginx:alpine
```

### Inspeccionar un volumen

```
docker volume inspect vol-nginx
```
