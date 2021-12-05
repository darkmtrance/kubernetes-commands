# Practica Test - PODs

- Ejecute el siguiente comando y obtendrá cuantos pods existen en el cluster de kubernetes (default) namespace.

```
kubectl get pods
```

- Ejecute el siguiente comando para crear un pod con imagen de nginx.

```
kubectl run nginx --image=nginx
```

- Ejecute el siguiente comando para verificar cuantos pods existen en el cluster de kubernetes (default) namespace.

```
kubectl get pods
```

- Ejecute el siguiente comando para verificar en que nodo se encuentra el pod creado

```
kubectl get pods -o wide
```

- Ejecute el siguiente comando y verificar el estado 

```
kubectl apply -f webapp.yaml

kubectl get pods

```

- Ejecute el siguiente comando para eliminar el pod 

```
kubectl delete pod webapp
```

o

```
kubectl delete -f webapp.yaml
```

- Ejecute el siguiente comando para generar el archivo yaml para crear un pod con nombre redis y con la imagen redis123

```
kubectl run redis --image=redis123 --dry-run=client -o yaml >> redis.yaml
kubectl apply -f redis.yaml
```

- Ejecute el siguiente comando para verificar el estado del pod

```
kubectl describe pod redis
```


- Ejecute el siguiente comando para editar el pod redis, modificando la imagen redis123 a redis


```
kubectl edit pod redis
```


