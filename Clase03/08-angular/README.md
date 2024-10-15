# Angular

### Crear contenedor

```
docker run -d \
    --name server-angular \
    --publish published=8888,target=80 \
    --mount type=volume,source=$(pwd -W)/dist/04-angular/browser,target=/usr/share/nginx/html \
    nginx:alpine
```

```
docker run -d `
    --name server-angular `
    --publish published=8888,target=80 `
    --mount type=volume,source=D:/Cursos/Docker_Kubernetes_Group14/Clase03/08-angular/dist/04-angular/browser,target=/usr/share/nginx/html `
    nginx:alpine
```
