# Carbide Helm Charts

### Available Helm Charts

```bash
NAME                            CHART VERSION   APP VERSION     DESCRIPTION
carbide-charts/airgapped-docs   0.1.55          0.1.8           Rancher Government Airgapped Docs
carbide-charts/heimdall2        0.1.45          0.1.1           Rancher Government Heimdall2 Tool
carbide-charts/rancher          2.12.4          v2.12.4         Install Rancher Server to manage Kubernetes clu...
carbide-charts/stigatron        0.4.0           0.4.0           Rancher Government Stigatron Extension
carbide-charts/stigatron-ui     0.3.0           0.3.0           Rancher Government Stigatron UI Extension
```

## How To Use (Connected Environments)

### For Helm Chart Repositories

```bash
# add and update the helm chart repository
helm repo add carbide-charts https://rancherfederal.github.io/carbide-charts
helm repo update

# view the charts in the helm chart repository
helm search repo carbide-charts

# example install of a helm chart
helm install <release-name> carbide-charts/<chart>
```

If you would like to do add the Carbide Helm Charts to the Rancher Manager Chart Catalog, so you are able to use the user interface to install them, please follow the steps in the [Rancher Manager Docs](https://ranchermanager.docs.rancher.com/how-to-guides/new-user-guides/helm-charts-in-rancher).

## How to Use (Airgapped Environments)

### For Helm Chart Repositories

#### On Connected Environment

```bash
# fetch the content from carbide charts hauler manifest
hauler store sync --filename https://raw.githubusercontent.com/rancherfederal/carbide-charts/refs/heads/main/carbide-charts.yaml

# save and output the content from the hauler store to tarball
hauler store save --filename carbide-charts.tar.zst
```

#### On Airgapped Environment

```bash
# load the content from the tarball to the hauler store
hauler store load --filename carbide-charts.tar.zst

# example install method with helm oci and hauler registry
hauler store serve registry
helm install <release-name> oci://<FQDN or IP>:<PORT>/hauler/<chart> --version <version>

# example install method with helm repo and hauler fileserver
hauler store serve fileserver
helm install <release-name> http://<FQDN or IP>:<PORT>/<chart>.tgz
```
