# Kubernetes

### Crear un pod

```
kubectl run pod-nginx --image=nginx:alpine
```

### Port-forward

```
kubectl port-forward pod-nginx 7000:80
```

### Comandos

```
kubectl version
kubectl api-resources
```
