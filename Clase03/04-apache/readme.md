# Apache

### Crear un volumen

```
docker volume create vol-apache
```

### Crear el contenedor

```
docker run -d \
    --name server-apache \
    -v vol-apache:/usr/local/apache2/htdocs \
    --publish published=8090,target=80 \
    httpd:2.4
```

```
docker run -d \
    --name server-apache \
    --mount type=volume,source=vol-apache,target=/usr/local/apache2/htdocs \
    --publish published=8090,target=80 \
    httpd:2.4
```

```
docker run -d `
    --name server-apache `
    --mount type=volume,source=vol-apache,target=/usr/local/apache2/htdocs `
    --publish published=8090,target=80 `
    httpd:2.4
```
