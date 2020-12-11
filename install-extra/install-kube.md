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

## Install in AWS Linux2

### Kubectl
[Kubectl instructions](https://kubernetes.io/docs/tasks/tools/install-kubectl/)
```
curl -LO https://storage.googleapis.com/kubernetes-release/release/`curl -s https://storage.googleapis.com/kubernetes-release/release/stable.txt`/bin/linux/amd64/kubectl
chmod +x ./kubectl
sudo mv ./kubectl /usr/bin/kubectl

#test
kubectl version --client
```

### Minikube
[Minikube instructions]((https://minikube.sigs.k8s.io/docs/start/)
```
curl -Lo minikube https://storage.googleapis.com/minikube/releases/latest/minikube-linux-amd64
chmod +x minikube
sudo mv minikube /usr/bin/

#test
minikube version

## sudo yum install conntrack -y

## run minikube
```


