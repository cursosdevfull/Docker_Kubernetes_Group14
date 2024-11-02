# Pods

### Ejecutar un manifiesto

```
kubectl apply -f <ruta y nombre del manifiesto>
```

### Eliminar un manifiesto

```
kubectl delete -f <ruta y nombre del manifiesto>
```

### Listar pods

```
kubectl get pods
kubectl get po
```

### Describir un pod

```
kubectl describe pod pod-nginx
```

### Visualizar los logs

```
kubectl logs pod-nginx
```

### Ingresar a contenedor

```
kubectl exec -it -- <programa a ejecutar>
kubectl exec -it -- <programa a ejecutar> -c <nombre contenedor>
```

### Listar pods con sus etiquetas

```
kubectl get po --show-labels
```

### Ver el manifiesto de un pod

```
kubectl get po <nombre pod> -o yaml
```
