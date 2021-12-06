# Practica Test - replicaset

- Ejecute el siguiente comando y obtendrá cuantos pods existen en el cluster de kubernetes (default) namespace.

```
kubectl get pods
```

- Ejecute el siguiente comando y obtendrá cuantos replicaset existen en el cluster de kubernetes (default) namespace.

```
kubectl get rs
```

- Ejecute el siguiente comando y verificar nuevamente cuantos replicaset existen

```
kubectl apply -f new-replicaset.yaml
kubectl get rs
```

- Ejecute el siguiente comando para verificar cuantos pods son DESIRED (Deseables) en el new-replica-set

```
kubectl get rs new-replica-set
```

- Cual es la imagen que utiliza los pods creados en el new-replica-set

```
kubectl get rs new-replica-set -o wide
```

- Verificar cuantos pods son READY en el new-replica-set
<!--Por qué crees que las POD no están READY-->

```
kubectl get rs new-replica-set
```

- Elimina cualquiera de los 4 PODs

```
kubectl delete pod new-replica-set-2czll
```

- ¿Cuántos POD existen ahora?

```
kubectl get pods
```

- ¿Por qué todavía quedan 4 PODs, incluso después de eliminar uno?

<!--replicaset asegura que la cantidad deseada de pods siempre se ejecute-->

- Hay un problema con el archivo replicaset-1.yaml, intente solucionarlo.

```
kubectl apply -f replicaset-1.yaml
```

- Hay un problema con el archivo replicaset-2.yaml, intente solucionarlo.

```
kubectl apply -f replicaset-2.yaml
```

- Eliminar los dos replicaset replicaset-1 y replicaset-2.

```
kubectl delete rs replicaset-1 replicaset-2
```

- Hay un problema en el replicaset new-replica-set usando el correcto imagen busybox, intente solucionarlo.

```
kubectl edit rs new-replica-set
```

- Escale el ReplicaSet a 5 PODs.

```
kubectl scale --replicas=5 rs/new-replica-set
```

Ahora reduzca la ReplicaSet a 2 PODs.

```
kubectl scale --replicas=2 rs/new-replica-set
```
