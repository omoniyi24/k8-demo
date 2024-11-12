# Minikube Kubernetes Commands

## Start Minikube and Check Status

```bash
minikube start --vm-driver=hyperkit 
minikube status
```

## Get Minikube Node's IP Address
```
minikube ip
```
## Get Basic Info about Kubernetes Components
```
kubectl get node
kubectl get pod
kubectl get svc
kubectl get all
```

## Get Extended Info about Components
```
kubectl get pod -o wide
kubectl get node -o wide
```

## Get Detailed Info about a Specific Component
* For a Service:
```
kubectl describe svc {svc-name}
```
* For a Pod:
```
kubectl logs {pod-name}
```

## Stop Your Minikube Cluster
```
minikube stop
```

## ⚠️ Known Issue - Minikube IP Not Accessible
If you can't access the NodePort service (e.g., webapp) using MinikubeIP:NodePort, use the following command:
```
minikube service webapp-service
```
for port forwarding
```
kubectl port-forward svc/webapp-service 8080:3000
```

