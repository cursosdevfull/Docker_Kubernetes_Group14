# Certificados

### Crear la llave privada

```
openssl genrsa -out curso14.key 2048
```

### Crear la solicitud

```
openssl req -new -key curso14.key -out curso14.csr -subj "/CN=curso14/O=developers"
```

### Generar el certificado final

```
openssl x509 -req -in curso14.csr -CA \\wsl.localhost\docker-desktop-data\data\kubeadm\pki\ca.crt -CAkey \\wsl.localhost\docker-desktop-data\data\kubeadm\pki\ca.key -CAcreateserial -out curso14.crt -days 365
```
