# Install microk8s on Ununti 18.04

## Install Packages

```
sudo snap install microk8s --classic
sudo snap alias microk8s.kubectl kubectl
```

## Enable Extensions

```
microk8s.enable dns dashboard ingress
```

## Create A Hello World Service

Create the POD.

```
wget https://github.com/omahoco/snippets/hello_world_pod.yaml 

kubectl create -f hello_world_pod.yaml
```

Create the service.

```
wget https://github.com/omahoco/snippets/hello_world_service.yaml

kubectl create -f hello_world_service.yaml
```

Create the ingress

```
wget https://github.com/omahoco/snippets/hello_world_ingress.yaml

kubectl create -f hello_world_ingress.yaml
```

