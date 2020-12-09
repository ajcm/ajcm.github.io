## Install Kubectl/Minikube

### Kubectl
[Kubectl instructions](https://kubernetes.io/docs/tasks/tools/install-kubectl/)
```
sudo apt-get update && sudo apt-get install -y apt-transport-https gnupg2 curl -y
curl -s https://packages.cloud.google.com/apt/doc/apt-key.gpg | sudo apt-key add -
echo "deb https://apt.kubernetes.io/ kubernetes-xenial main" | sudo tee -a /etc/apt/sources.list.d/kubernetes.list
sudo apt-get update -y
sudo apt-get install -y kubectl

#test
kubectl version --client
```

### Minikube
[Minikube instructions]((https://minikube.sigs.k8s.io/docs/start/)
```
curl -LO https://storage.googleapis.com/minikube/releases/latest/minikube_latest_amd64.deb
sudo dpkg -i minikube_latest_amd64.deb

minikube version
```

---