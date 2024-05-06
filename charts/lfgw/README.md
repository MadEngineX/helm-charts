# lfgw-chart

Helm Chart to deploy [LFGW](https://github.com/weisdd/lfgw)

## Add a chart helm repository

Go to Kubernetes cluster.

Add a chart helm repository with follow commands:

```bash 
helm repo add m8x https://MadEngineX.github.io/helm-charts/

helm repo update
```

## Deploy LFGW

```bash 
helm upgrade --install lfgw m8x/lfgw
```

You can also deploy [lfgw-config-operator](https://github.com/MadEngineX/lfgw-config-operator) by enabling subchart in values: 
```yaml 
lfgw-operator-chart:
  enabled: false
```
If you want to use __lfgw-config-operator__, specify `aclConfigMap.create: false`. Also, due to limitation on operator side you need to deploy [stakater/Reloader](https://github.com/stakater/Reloader) to rollout LFWG Deployment on ConfigMap changes.