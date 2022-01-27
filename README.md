# Helm charts

This repository stores Helm chart tarballs authored by Luigi Di Fraia. Actual development of these Helm charts takes place in this [Helm chart repo](https://github.com/luigidifraia/helm-charts).

## Using charts from this repo

Make Helm aware of the [Helm chart repository](https://luigidifraiawork.github.io/helm-charts), so you will be able to install charts from it without having to use a long URL name:

```bash
helm repo add luigidifraia https://luigidifraiawork.github.io/helm-charts
helm repo update
```

You can then list the available charts with:

```bash
helm search repo luigidifraia
```
