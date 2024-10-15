# Drupal

### Crear un red

```
docker network create net-drupal -d bridge
```

### Crear volumenes nombrados

```
docker volume create vol-drupal-mysql
docker volume create vol-drupal-files
```

### Crear el contenedor de MySQL

```
docker run -d --name server-drupal-mysql -e MYSQL_ROOT_PASSWORD=12345 -e MYSQL_USER=user -e MYSQL_PASSWORD=12345 -e MYSQL_DATABASE=wp-db -v vol-drupal-mysql:/var/lib/mysql --network net-drupal mysql:8
```

### Crear el contenedor de Drupal

```
docker run -d --name server-drupal \
    -p 9000:80 \
    -v vol-drupal-files:/var/www/html \
    --network net-drupal \
    drupal
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
