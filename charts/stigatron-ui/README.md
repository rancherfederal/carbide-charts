STIGATRON-UI Chart
----------------------------------------------


| Type | Chart Version | App Version |
| ---- | ------------- | ----------- |
| application | `0.1.0` | `0.1.17` |

## Installing the Chart
```bash
helm install -n carbide-stigatron-system --create-namespace stigatron-ui carbide-charts/stigatron-ui
```
```bash
helm status -n carbide-stigatron-system stigatron-ui
```

## Uninstalling the Chart
```bash
helm uninstall -n carbide-stigatron-system stigatron-ui carbide-charts/stigatron-ui
```

## Configuration

The following table lists the configurable parameters of the Stigatron-ui chart and their default values.

| Parameter | Default | Description |
| --------- | ------- | ----------- |
| `replicaCount` | `1` |  |
| `UIPluginNamespace` | `"cattle-ui-plugin-system"` |  |
| `image.pullPolicy` | `"Always"` |  |
| `image.tag` | `"0.1.0"` |  |
| `image.name` | `"carbide/stigatron-ui"` |  |
| `imagePullSecrets` | `[]` |  |
| `nameOverride` | `""` |  |
| `fullnameOverride` | `""` |  |
| `serviceAccount.create` | `true` |  |
| `serviceAccount.annotations` | `{}` |  |
| `serviceAccount.name` | `""` |  |
| `podAnnotations` | `{}` |  |
| `podSecurityContext` | `{}` |  |
| `service.type` | `"ClusterIP"` |  |
| `service.port` | `80` |  |
| `resources` | `{}` |  |
| `nodeSelector` | `{}` |  |
| `tolerations` | `[]` |  |
| `affinity` | `{}` |  |
| `global.cattle.systemDefaultRegistry` | `"rgcrprod.azurecr.us"` |  |

