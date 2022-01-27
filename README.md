# helm-charts

![Release](https://github.com/luigidifraia/helm-charts/workflows/Release/badge.svg)

A Helm chart repo for useful charts.

## Using charts from this repo

Make Helm aware of the [Helm chart repository](https://luigidifraia.github.io/helm-charts/), so you will be able to install charts from it without having to use a long URL name:
```
helm repo add luigidifraia https://luigidifraiawork.github.io/helm-charts/
helm repo update
```
You can then list the available charts with:
```
helm search repo luigidifraia
```
### Deployment example
For deploying a Jupyter Lab instance you can use:
```
helm upgrade --namespace <namespace> --install jupyter luigidifraia/jupyter \
     --set "image.repository=jupyter/datascience-notebook" \
     --set "storage.capacity=10Gi" \
     --set "nodeSelector.component=jupyter" \
     --wait
```
To delete it:
```
helm delete jupyter --namespace <namespace>
```
