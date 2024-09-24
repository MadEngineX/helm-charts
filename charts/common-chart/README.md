# common-chart

Helm Chart to deploy several simple resources for education course (https://stepik.org/course/188289/promo)

## Add a chart helm repository

Go to Kubernetes cluster.

Add a chart helm repository with follow commands:

```bash 
helm repo add m8x https://MadEngineX.github.io/helm-charts/

helm repo update
```

## Deploy LFGW

```bash 
helm upgrade --install <release_name> m8x/lfgw <-f valyes.yaml>
```