## Install Kubectl/Minikube



### Test Kubernetes

```
kubectl create deployment hello-minikube --image=k8s.gcr.io/echoserver:1.4
kubectl expose deployment hello-minikube --type=NodePort --port=8080

kubectl get services hello-minikube
minikube service hello-minikube

kubectl port-forward service/hello-minikube 7080:8080
```
---