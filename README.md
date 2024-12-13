# Basic-k8s-cluster
In this repository, I developed a basic k8s cluster, with 4 configuration files., using configMaps, secrets, service and deployments.

# How to run this cluster

You need to have installed on your computer(Windows) [Docker Desktop](https://www.docker.com/products/docker-desktop/).

You need to install [**minikube**](https://minikube.sigs.k8s.io/docs/start/?arch=%2Fwindows%2Fx86-64%2Fstable%2F.exe+download)

You must have [**kubectl**](https://kubernetes.io/docs/tasks/tools/install-kubectl-windows/).

## After installing those you need to have Docker running.

In the PowerShell you need to type
```
minikube start --driver=docker
```

## After you run minikube, you will need to run the following commands:

```
kubectl apply -f mongo-config.yaml
```
```
kubectl apply -f mongo-service.yaml
```
```
kubectl apply -f mongo.yaml
```
```
kubectl apply -f webapp.yaml
```
In that same order.

## You will have your cluster running, so you will need to:

- Get the minikube IP with the following command in the CMD:
```
minikube ip
```

## To connect to the webapp you will need to type the minikubeip:30100

### In case that the webapp doesn't run at the moment of doing that, you must run the following command in the CMD:

```
minikube service webapp-service
```

# To stop the K8s cluster, you must type the command:
```
minikube stop
```
