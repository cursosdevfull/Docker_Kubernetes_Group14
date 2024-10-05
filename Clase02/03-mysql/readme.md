# MySQL

### Crear contenedor

```
docker run -d --name server-mysql01 -p 3310:3306 mysql:8
docker run -d --name server-mysql01 -e MYSQL_ROOT_PASSWORD=12345 -p 3310:3306 mysql:8
```

### Crear cliente

```
docker run -d --name client-mysql -p 8080:80 -e PMA_ARBITRARY=1 phpmyadmin:5.2.1
```

### Crear contenedor con usuario no administrador

```
docker run -d --name server-mysql02 -e MYSQL_ROOT_PASSWORD=12345 -e MYSQL_USER=user -e MYSQL_PASSWORD=user12345 -e MYSQL_DATABASE=db -p 3311:3306 mysql:8
```

### Crear contenedor usando variables de entorno desde un archivo

```
docker run -d --name server-mysql03 -e MYSQL_ROOT_PASSWORD=12345 --env-file=environment.txt -p 3312:3306 mysql:8

```
