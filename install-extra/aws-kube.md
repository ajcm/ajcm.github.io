## Install AWS Kubectl/Minikube

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

