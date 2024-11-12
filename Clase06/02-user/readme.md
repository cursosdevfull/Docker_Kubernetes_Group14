# Usuarios

### Copiar

- Copiar el certificado y la llaver privada (crt, key) en la carpeta de kubernetes llamada `.kube`
- Ubicarnos en la carpeta `.kube`

### Crear el usuario

```
kubectl config set-credentials curso14 --client-certificate=curso14.crt --client-key=curso14.key
```
