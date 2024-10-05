# Postgres

### Crear el contenedor

```
docker run -d --name server-postgres01 -e POSTGRES_PASSWORD=12345 postgres:alpine3.20
```

### Crear un cliente de postgres

```
docker run -d --name client-postgres -p 8090:80 -e PGADMIN_DEFAULT_EMAIL=sergiohidalgocaceres@gmail.com -e PGADMIN_DEFAULT_PASSWORD=54321 dpage/pgadmin4:8
```
