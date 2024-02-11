# kubernetes
# Install EC2 INSTANCE WITH T2.MEDIUM
Because while installting minikube free tier will not support 
![image](https://github.com/sowmiya429/kubernetes/assets/80743760/ed0f4b0e-76d8-42c5-8353-76cfb0704780)
# Add security group
![image](https://github.com/sowmiya429/kubernetes/assets/80743760/b7f8f345-c228-4547-b4da-c2149c6698d8)
# Connect EC2 instance
![image](https://github.com/sowmiya429/kubernetes/assets/80743760/7e4b0c66-ac63-45a5-aadb-1c5b7cd26a2f)
# log in to root user
![image](https://github.com/sowmiya429/kubernetes/assets/80743760/6331e479-89e6-4615-9bd3-808b10061a92)
# update the ec2 instance
![image](https://github.com/sowmiya429/kubernetes/assets/80743760/8aadb074-88ec-4920-b857-e085552d2523)
```
sudo apt update -y
```
# Install kubectl
```
curl -LO https://storage.googleapis.com/kubernetes-release/release/`curl -s https://storage.googleapis.com/kubernetes-release/release/stable.txt`/bin/linux/amd64/kubectl
```
```
sudo mv ./kubectl /usr/local/bin/kubectl
```
# Install dockerchmod +x ./kubectl
```
sudo apt-get update && \
    sudo apt-get install docker.io -y
```
# Install minikube
```
curl -Lo minikube https://storage.googleapis.com/minikube/releases/latest/minikube-linux-amd64 && chmod +x minikube && sudo mv minikube /usr/local/bin/
```
# Check whether minikube installed or not. Check the version
```
minikube version
```
# Kubernetes v1.20.0 requires conntrack to be installed in root’s path. So let’s install conntrack
```
sudo apt install conntrack
```
# installing docker shim
```
git clone https://github.com/Mirantis/cri-dockerd.git
```
# install the crictl
```
VERSION="v1.24.1"
curl -L https://github.com/kubernetes-sigs/cri-tools/releases/download/$VERSION/crictl-${VERSION}-linux-amd64.tar.gz --output crictl-${VERSION}-linux-amd64.tar.gz
sudo tar zxvf crictl-$VERSION-linux-amd64.tar.gz -C /usr/local/bin
rm -f crictl-$VERSION-linux-amd64.tar.gz
```
# using WGET
```
VERSION="v1.24.1"
wget https://github.com/kubernetes-sigs/cri-tools/releases/download/$VERSION/crictl-$VERSION-linux-amd64.tar.gz
sudo tar zxvf crictl-$VERSION-linux-amd64.tar.gz -C /usr/local/bin
rm -f crictl-$VERSION-linux-amd64.tar.gz
```
# Starting minikube
```
minikube start --vm-driver=none
```

# start minikube forcefully on docker
```
minikube start --force --driver=docker
```
