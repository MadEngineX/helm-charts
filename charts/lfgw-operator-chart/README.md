# lfgw-operator-chart

Helm Chart to deploy [lfgw-config-operator](https://github.com/MadEngineX/lfgw-config-operator)

## Add a chart helm repository

Go to Kubernetes cluster.

Add a chart helm repository with follow commands:

```bash 
helm repo add m8x https://MadEngineX.github.io/helm-charts/

helm repo update
```

## Deploy lfgw-config-operator

```bash 
helm upgrade --install lfgw-operator m8x/lfgw-operator-chart 
```