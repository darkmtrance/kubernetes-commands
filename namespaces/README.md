# Practica Test - namespaces

- ¿Cuántos Namespaces existen en el sistema?

```
kubectl get ns
```

- Crear el namespace finance

```
kubectl create ns finance
```

- Crear un POD en el finance namespace.
Nombre: ```redis```
Nombre de la Imagen: ```redis```

```
kubectl run redis --image=redis -n finance
```
