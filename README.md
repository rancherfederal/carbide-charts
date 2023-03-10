# Rancher Government Carbide Helm Charts

Still a WIP!

## How To Use (Connected Environments)

```
helm repo add carbide-charts https://rancherfederal.github.io/carbide-charts
helm repo update
helm search repo carbide-charts
helm install example-release carbide-charts/<chart>
```

If you would like to do add the carbide-charts to the Rancher Manager Chart Catalog, please follow the steps in the [Rancher Manager Docs](https://ranchermanager.docs.rancher.com/how-to-guides/new-user-guides/helm-charts-in-rancher/create-apps#docusaurus_skipToContent_fallback) and use the following chart catalog Git Repo URL with the branch name of main:

```
https://github.com/rancherfederal/carbide-charts.git
```

## How to Use (Airgaped Environments)

### On Connected Environment

```
helm repo add carbide-charts https://rancherfederal.github.io/carbide-charts
helm repo update
helm search repo carbide-charts
helm pull carbide-charts/<chart>
```

Take the resulting `tgz` file over the airgap.
    
### On Airgapped Environment

```
helm install example-release <chart-example>.tgz
```
