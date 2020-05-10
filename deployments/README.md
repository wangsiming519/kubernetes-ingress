# Installation

This folder includes Kubernetes manifests for installing NGINX or NGINX Plus Ingress controller. Read the installation instructions [here](https://docs.nginx.com/nginx-ingress-controller/installation/).


# you can also follow the below steps to install 

```
git clone https://github.com/wangsiming519/kubernetes-ingress.git
cd kubernetes-ingress/deployments
git checkout v1.7.0

kubectl apply -f common/ns-and-sa.yaml
kubectl apply -f rbac/rbac.yaml
kubectl apply -f common/default-server-secret.yaml
kubectl apply -f common/nginx-config.yaml
kubectl apply -f ../examples/opentracing/nginx-config.yaml
kubectl apply -f deployment/nginx-ingress.yaml
kubectl create -f service/nodeport.yaml
```


