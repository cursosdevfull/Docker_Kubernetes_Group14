# Wordpress

### Crear un red

```
docker network create net-wp -d bridge
```

### Crear volumenes nombrados

```
docker volume create vol-wp-mysql
docker volume create vol-wp-files
```

### Crear el contenedor de MySQL

```
docker run -d --name server-wp-mysql -e MYSQL_ROOT_PASSWORD=12345 -e MYSQL_USER=user -e MYSQL_PASSWORD=12345 -e MYSQL_DATABASE=wp-db -v vol-wp-mysql:/var/lib/mysql --network net-wp mysql:8
```

### Crear el contenedor de WordPress

```
docker run -d --name server-wp \
    -e WORDPRESS_DB_HOST=server-wp-mysql \
    -e WORDPRESS_DB_USER=user \
    -e WORDPRESS_DB_PASSWORD=12345 \
    -e WORDPRESS_DB_NAME=wp-db \
    -p 9000:80 \
    -v vol-wp-files:/var/www/html \
    --network net-wp \
    wordpress
```

### En PowerShell

```
docker run -d --name server-wp `
    -e WORDPRESS_DB_HOST=server-wp-mysql `
    -e WORDPRESS_DB_USER=user `
    -e WORDPRESS_DB_PASSWORD=12345 `
    -e WORDPRESS_DB_NAME=wp-db `
    -p 9000:80 `
    -v vol-wp-files:/var/www/html `
    --network net-wp `
    wordpress
```
