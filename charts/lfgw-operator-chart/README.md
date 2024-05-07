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

Install CRD:
```bash
kubectl apply -f https://raw.githubusercontent.com/MadEngineX/lfgw-config-operator/main/config/crd/bases/controls.lfgw.io_acls.yaml
```

Deploy Helm release:
```bash 
helm upgrade --install lfgw-operator m8x/lfgw-operator-chart 
```