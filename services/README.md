# Practica Test - services

- ¿Cuántos servicios existen en el sistema?

```
kubectl get svc
```

- ¿Cuál es el tipo de servicio de Kubernetes predeterminado?

```
kubectl get svc kubernetes
```

- ¿Qué está configurado como targetPort en el servicio de kubernetes?

```
kubectl describe svc kubernetes
```

- ¿Cuántas etiquetas están configuradas en el servicio de kubernetes?

```
kubectl describe svc kubernetes
```

- ¿Cuántos Endpoints se adjuntan en el servicio de kubernetes?

```
kubectl get ep
```

- Ejecute el siguiente comando.

```
kubectl apply -f deploy_example.yaml
```

- Crear un nuevo servicio para acceder a la aplicación web utilizando el archivo service.yaml

Nombre: ```webapp-service```
Tipo: ```NodePort```
targetPort: ```8080```
port: ```8080```
nodePort: ```30080```
selector: ```simple-webapp```

```
kubectl apply -f service.yaml
```