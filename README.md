# Rancher Government Carbide Helm Charts

Still a WIP!

## How To Use (Internet)

```
helm repo add carbide-charts https://rancherfederal.github.io/carbide-charts
helm repo update
helm search repo carbide-charts
helm install example-release carbide-charts/<chart>
```

## How to Use (Airgap)

### On Connected Device

```
helm repo add carbide-charts https://rancherfederal.github.io/carbide-charts
helm repo update
helm search repo carbide-charts
helm pull carbide-charts/<chart>
```

Take the resulting `tgz` file over the airgap.
    
### On Airgapped Device

```
helm install example-release <chart-x.y.z>.tgz
```
