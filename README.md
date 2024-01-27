# kubernetes
# Install EC2 INSTANCE
![image](https://github.com/sowmiya429/kubernetes/assets/80743760/53081ca9-ec7e-4198-9aad-5a6adf7cdce6)
Now update the EC2 Instance
![image](https://github.com/sowmiya429/kubernetes/assets/80743760/25c4e7d0-8b46-4685-bf24-011c6ad170c3)
Now install KUBECTL
```
 curl -LO https://storage.googleapis.com/kubernetes-release/release/`curl -s https://storage.googleapis.com/kubernetes-release/release/stable.txt`/bin/linux/amd64/kubectl
```
# Make teh KUBECTL the binary executable
```
chmod +x ./kubectl
```
# Move binary into your path
```
sudo mv ./kubectl /usr/local/bin/kubectl
```
# To ensure the kubectl installed
```
kubectl version --client
```

