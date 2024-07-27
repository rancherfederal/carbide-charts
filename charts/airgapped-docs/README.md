Airgapped-Docs Chart
----------------------------------------------


| Type | Chart Version | App Version |
| ---- | ------------- | ----------- |
| application | `0.1.51` | `0.1.6` |

## Installing the Chart
```bash
helm install -n carbide-docs-system --create-namespace airgapped-docs carbide-charts/airgapped-docs
```
```bash
helm status -n carbide-docs-system airgapped-docs
```

## Uninstalling the Chart
```bash
helm uninstall -n carbide-docs-system airgapped-docs
```

## Configuration

The following table lists the configurable parameters of the Airgapped-docs chart and their default values.

| Parameter | Default | Description |
| --------- | ------- | ----------- |
| `global.cattle.systemDefaultRegistry` | `"rgcrprod.azurecr.us"` |  |
| `images.carbide.name` | `"carbide/carbide-docs"` |  |
| `images.carbide.tag` | `"0.1.6"` |  |
| `docs.kubernetes.enabled` | `true` |  |
| `docs.kubernetes.uid` | `65532` |  |
| `docs.kubernetes.image.name` | `"carbide/kubernetes-cncf-docs"` |  |
| `docs.kubernetes.image.tag` | `"0.1.6"` |  |
| `docs.rancher.enabled` | `true` |  |
| `docs.rancher.uid` | `65532` |  |
| `docs.rancher.image.name` | `"carbide/rancher-docs"` |  |
| `docs.rancher.image.tag` | `"0.1.6"` |  |
| `docs.rke2.enabled` | `true` |  |
| `docs.rke2.uid` | `65532` |  |
| `docs.rke2.image.name` | `"carbide/rke2-docs"` |  |
| `docs.rke2.image.tag` | `"0.1.6"` |  |
| `docs.k3s.enabled` | `true` |  |
| `docs.k3s.uid` | `65532` |  |
| `docs.k3s.image.name` | `"carbide/k3s-docs"` |  |
| `docs.k3s.image.tag` | `"0.1.6"` |  |
| `docs.neuvector.enabled` | `true` |  |
| `docs.neuvector.uid` | `100` |  |
| `docs.neuvector.image.name` | `"carbide/neuvector-docs"` |  |
| `docs.neuvector.image.tag` | `"0.1.6"` |  |
| `docs.fleet.enabled` | `true` |  |
| `docs.fleet.uid` | `65532` |  |
| `docs.fleet.image.name` | `"carbide/fleet-docs"` |  |
| `docs.fleet.image.tag` | `"0.1.6"` |  |
| `docs.longhorn.enabled` | `true` |  |
| `docs.longhorn.uid` | `65532` |  |
| `docs.longhorn.image.name` | `"carbide/longhorn-docs"` |  |
| `docs.longhorn.image.tag` | `"0.1.6"` |  |
| `docs.kubewarden.enabled` | `true` |  |
| `docs.kubewarden.uid` | `65532` |  |
| `docs.kubewarden.image.name` | `"carbide/kubewarden-docs"` |  |
| `docs.kubewarden.image.tag` | `"0.1.6"` |  |
| `docs.carbide.enabled` | `true` |  |
| `docs.carbide.uid` | `65532` |  |
| `docs.carbide.image.name` | `"carbide/carbide-docs"` |  |
| `docs.carbide.image.tag` | `"0.1.6"` |  |
| `docs.elemental.enabled` | `true` |  |
| `docs.elemental.uid` | `65532` |  |
| `docs.elemental.image.name` | `"carbide/elemental-docs"` |  |
| `docs.elemental.image.tag` | `"0.1.6"` |  |
| `docs.harvester.enabled` | `true` |  |
| `docs.harvester.uid` | `65532` |  |
| `docs.harvester.image.name` | `"carbide/harvester-docs"` |  |
| `docs.harvester.image.tag` | `"0.1.6"` |  |
| `docs.rancherdesktop.enabled` | `true` |  |
| `docs.rancherdesktop.uid` | `65532` |  |
| `docs.rancherdesktop.image.name` | `"carbide/rancher-desktop-docs"` |  |
| `docs.rancherdesktop.image.tag` | `"0.1.6"` |  |

