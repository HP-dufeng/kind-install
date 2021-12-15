

## Create cluster
```
kind create cluster --name CLUSTER_NAME --config ./cluster-config.yaml

kind get clusters

kind delete cluster --name CLUSTER_NAME
```


## install metallb
```
kubectl apply -f namespace.yaml
kubectl apply -f metallb-configmap.yaml
kubectl apply -f metallb.yaml

```

## install ingress-nginx
```
kind load docker-image k8s.gcr.io/ingress-nginx/controller:v1.1.0 k8s.gcr.io/ingress-nginx/kube-webhook-certgen:v1.1.1

kubectl apply -f deploy.yaml
```