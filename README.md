## Create cluster with exposed ingress ports
```console
minikube start --cpus=max --memory=5g --addons=ingress --ports=80:80,443:443
```
## Install cert-manager, and LE cluster issuers
```console
kubectl apply -f https://github.com/cert-manager/cert-manager/releases/download/v1.15.0/cert-manager.yaml
```
```console
kubectl apply -f cluster-issuer.yaml
```
## Deploy hello-world app
```console
kubectl apply -f hello-world.yaml
```
