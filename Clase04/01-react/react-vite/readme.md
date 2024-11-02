# React

### Crear contenedor

```
docker run -d \
    --name server-react \
    --publish published=8888,target=80 \
    --mount type=bind,source=$(pwd -W)/dist,target=/usr/share/nginx/html \
    nginx:alpine
```

```
docker run -d `
    --name server-react `
    --publish published=8888,target=80 `
    --mount type=bind,source=D:/Cursos/Docker_Kubernetes_Group14/Clase04/01-react/react-vite/dist,target=/usr/share/nginx/html `
    nginx:alpine
```
