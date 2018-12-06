# Digituz Kubernetes Config

First, you will need to configure [the NGINX Ingress Controller for Kubernetes](https://github.com/kubernetes/ingress-nginx):

```bash
kubectl apply -f core/mandatory.yaml
kubectl create -f core/cloud-generic.yaml
```

With that in place, you can start deploying applications:

```bash
kubectl create -f krebseng/krebseng-deployment.yaml
kubectl create -f krebseng/krebseng-service.yaml
kubectl create -f krebseng/krebseng-ingress.yaml
```
