# kind-ingress

## Prerequisites
- kind

## Instructions

### Create Cluster
```bash
kind create cluster --config=config.yaml
```

### Deploy Ingress Controller
```bash
kubectl apply -f https://raw.githubusercontent.com/kubernetes/ingress-nginx/main/deploy/static/provider/kind/deploy.yaml
```

### Deploy Application
```bash
kubectl apply -f example.yaml

# Test:
curl localhost/foo/hostname
curl localhost/bar/hostname
```
