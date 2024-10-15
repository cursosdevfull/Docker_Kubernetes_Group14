# NGINX - Volúmen de tipo Host

### Crear el volúmen usando la ruta relativa (Git Bash)

```
docker run -d --name server-nginx -p 9000:80 -v $(pwd -W)/www:/usr/share/nginx/html nginx:alpine
```
