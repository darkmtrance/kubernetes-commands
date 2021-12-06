# Practica Test - deployment

- Ejecute el siguiente comando y obtendrá cuantos pods existen en el cluster de kubernetes (default) namespace.

```
kubectl get pods
```

- Ejecute el siguiente comando y obtendrá cuantos replicaset existen en el cluster de kubernetes (default) namespace.

```
kubectl get rs
```

- Ejecute el siguiente comando y obtendrá cuantos deployments existen en el cluster de kubernetes (default) namespace.

```
kubectl get deploy
```

- Ejecute el siguiente comando y  y verificar nuevamente cuantos deployments existen

```
kubectl apply -f deploy.yaml
kubectl get deploy
```


- Verificar cuantos replicaset existen

```
kubectl get rs
```

- Verificar cuantos pods existen

```
kubectl get pods
```

- Hay un problema en el deployment frontend-deployment, intente solucionarlo.
<!-- usar el rolling updates - kubectl set image - kubectl rollout  -->

```
kubectl apply -f deploy.yaml
```

- Crear una nueva implementación con los siguientes atributos utilizando su propio archivo de definición de implementación (deployment file).

Nombre: ```httpd-frontend```
Replicas: ```3```
Imagen: ```httpd:2.4-alpine```
