# NGINX - Volúmen de tipo Host

### Crear el volúmen usando la ruta relativa (Git Bash)

```
docker run -d --name server-nginx -p 9000:8080 -v $(pwd -W)/www:/app -v $(pwd -W)/configuration/nginx.conf:/etc/nginx/conf.d/default.conf nginx:alpine
```
