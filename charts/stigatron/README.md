## STIGATRON Chart

| Type        | Chart Version | App Version |
| ----------- | ------------- | ----------- |
| application | `0.4.0`       | `0.4.0`     |

## Installing the Chart

```bash
helm install -n carbide-stigatron-system stigatron carbide-charts/stigatron
```

```bash
helm status -n carbide-stigatron-system stigatron
```

## Uninstalling the Chart

```bash
helm uninstall -n carbide-stigatron-system stigatron
```

## Configuration

The following table lists the configurable parameters of the Stigatron chart and their default values.

| Parameter                                              | Default                                | Description      |
| ------------------------------------------------------ | -------------------------------------- | ---------------- |
| `complianceOperator.image.name`                        | `"carbide/compliance-operator"`        |                  |
| `complianceOperator.image.tag`                         | `"0.1.0"`                              |                  |
| `complianceOperator.imagePullPolicy`                   | `"Always"`                             |                  |
| `complianceOperator.serviceAccountName`                | `"stigatron"`                          |                  |
| `heimdallOperator.image.name`                          | `"carbide/heimdall-operator"`          |                  |
| `heimdallOperator.image.tag`                           | `"0.1.0"`                              |                  |
| `heimdallOperator.imagePullPolicy`                     | `"Always"`                             |                  |
| `heimdallOperator.serviceAccountName`                  | `"stigatron"`                          |                  |
| `heimdallOperator.database.port`                       | `"5432"`                               |                  |
| `heimdallOperator.database.name`                       | `"heimdall"`                           |                  |
| `heimdallOperator.database.user`                       | `"postgres"`                           |                  |
| `heimdallOperator.database.password`                   | `"password"`                           |                  |
| `heimdallOperator.database.sslMode`                    | `false`                                |                  |
| `hook.image.name`                                      | `"carbide/stigatron-hook"`             |                  |
| `hook.image.tag`                                       | `"0.1.0"`                              |                  |
| `hook.imagePullPolicy`                                 | `"Always"`                             |                  |
| `rbac.roleName`                                        | `"compliance-operator"`                |                  |
| `rbac.roleBindingName`                                 | `"compliance-operator"`                |                  |
| `alert.enabled`                                        | `false`                                |                  |
| `heimdall2.databasePort`                               | `5432`                                 |                  |
| `heimdall2.databaseName`                               | `"heimdall"`                           |                  |
| `heimdall2.jwtSecret`                                  | `"abcde12345"`                         |                  |
| `heimdall2.heimdall.image.name`                        | `"carbide/heimdall2"`                  |                  |
| `heimdall2.heimdall.image.tag`                         | `"0.1.0"`                              |                  |
| `heimdall2.postgres.enabled`                           | `true`                                 |                  |
| `heimdall2.postgres.user`                              | `"postgres"`                           |                  |
| `heimdall2.postgres.password`                          | `"password"`                           |                  |
| `heimdall2.postgres.persistence.enabled`               | `false`                                |                  |
| `global.cattle.systemDefaultRegistry`                  | `"rgcrprod.azurecr.us"`                |                  |
| `heimdall2.proxy.imagePullPolicy`                      | `"IfNotPresent"`                       |                  |
| `heimdall2.proxy.image.name`                           | `"carbide/heimdall-proxy"`             |                  |
| `heimdall2.proxy.image.tag`                            | `"0.1.0"`                              |                  |
| `heimdall2.proxy.port`                                 | `8080`                                 |                  |
| `heimdall2.proxy.service.type`                         | `"ClusterIP"`                          |                  |
| `heimdall2.proxy.service.port`                         | `80`                                   |                  |
| `heimdall2.postgres.image.name`                        | `"carbide/postgres"`                   |                  |
| `heimdall2.postgres.image.tag`                         | `"13"`                                 |                  |
| `heimdall2.postgres.imagePullPolicy`                   | `"IfNotPresent"`                       |                  |
| `heimdall2.postgres.port`                              | `5432`                                 |                  |
| `heimdall2.postgres.service.type`                      | `"ClusterIP"`                          |                  |
| `heimdall2.postgres.service.port`                      | `5432`                                 |                  |
| `heimdall2.postgres.persistence.persistentVolumeClaim` | `""`                                   |                  |
| `heimdall2.postgres.persistence.storageClassName`      | `""`                                   |                  |
| `heimdall2.postgres.persistence.storageRequest`        | `"10Gi"`                               |                  |
| `heimdall2.postgres.persistence.accessMode`            | `"ReadWriteOnce"`                      |                  |
| `heimdall2.postgres.podAnnotations`                    | `{}`                                   |                  |
| `heimdall2.postgres.securityContext`                   | `{}`                                   |                  |
| `heimdall2.postgres.resources`                         | `{}`                                   |                  |
| `heimdall2.postgres.nodeSelector`                      | `{}`                                   |                  |
| `heimdall2.postgres.affinity`                          | `{}`                                   |                  |
| `heimdall2.postgres.tolrations`                        | `{}`                                   |                  |
| `heimdall2.heimdall.kubernetesRequiredPermissions`     | `["compliance.cattle.io,scans,,list"]` |                  |
| `heimdall2.heimdall.paths.public`                      | `""`                                   |                  |
| `heimdall2.heimdall.paths.vue`                         | `""`                                   |                  |
| `heimdall2.heimdall.paths.router`                      | `""`                                   |                  |
| `heimdall2.heimdall.paths.axios`                       | `""`                                   |                  |
| `heimdall2.heimdall.rcidf.name`                        | `"carbide/rcidf"`                      |                  |
| `heimdall2.heimdall.rcidf.tag`                         | `"0.1.0"`                              |                  |
| `heimdall2.heimdall.databaseName`                      | `"heimdall"`                           |                  |
| `heimdall2.heimdall.image.path`                        | `"0.1.0"`                              |                  |
| `heimdall2.heimdall.port`                              | `8080`                                 |                  |
| `heimdall2.heimdall.service.type`                      | `"ClusterIP"`                          |                  |
| `heimdall2.heimdall.service.port`                      | `80`                                   |                  |
| `heimdall2.heimdall.jwtExpireTime`                     | `"1d"`                                 |                  |
| `heimdall2.heimdall.fleetNamespace`                    | `"cattle-fleet-system"`                |                  |
| `heimdall2.heimdall.rancherNamespace`                  | `"cattle-system"`                      |                  |
| `heimdall2.heimdall.localLoginDisabled`                | `true`                                 |                  |
| `heimdall2.heimdall.apiKeySecret`                      | `""`                                   |                  |
| `heimdall2.heimdall.jwtSecret`                         | `""`                                   |                  |
| `heimdall2.heimdall.nodeEnv`                           | `"production"`                         | leave it to this |
| `heimdall2.heimdall.adminEmail`                        | `"admin@heimdall.local"`               |                  |
| `heimdall2.heimdall.adminPassword`                     | `""`                                   |                  |
| `heimdall2.heimdall.podAnnotations`                    | `{}`                                   |                  |
| `heimdall2.heimdall.selectorLabels`                    | `{}`                                   |                  |
| `heimdall2.heimdall.podSecurityContext`                | `{}`                                   |                  |
| `heimdall2.heimdall.securityContext`                   | `{}`                                   |                  |
| `heimdall2.heimdall.resources`                         | `{}`                                   |                  |
| `heimdall2.heimdall.nodeSelector`                      | `{}`                                   |                  |
| `heimdall2.heimdall.tolerations`                       | `[]`                                   |                  |
| `heimdall2.heimdall.affinity`                          | `{}`                                   |                  |
| `heimdall2.global.cattle.systemDefaultRegistry`        | `"rgcrprod.azurecr.us"`                |                  |
