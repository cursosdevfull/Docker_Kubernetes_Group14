# MYSQL - Volúmen de tipo Host

### Crear el volúmen usando la ruta absoluta

```
docker run -d --name server-mysql -e MYSQL_ROOT_PASSWORD=12345 -v D:\\Cursos\\Docker_Kubernetes_Group14\\Clase03\\volúmenes\\host\\mysql\\data-mysql:/var/lib/mysql mysql:8
```

### Crear el volúmen usando la ruta relativa (Git Bash)

```
docker run -d --name server-mysql -e MYSQL_ROOT_PASSWORD=12345 -v $(pwd -W)/data-mysql:/var/lib/mysql mysql:8
```

### Crear el volúmen usando la ruta relativa (Bash, SH)

```
docker run -d --name server-mysql -e MYSQL_ROOT_PASSWORD=12345 -v $(pwd)/data-mysql:/var/lib/mysql mysql:8
```

### Crear el volúmen usando la ruta relativa (PowerShell)

```
docker run -d --name server-mysql -e MYSQL_ROOT_PASSWORD=12345 -v ${PWD}/data-mysql:/var/lib/mysql mysql:8
```
