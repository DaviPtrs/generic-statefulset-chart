# statefulset-app

![Version: 0.1.0](https://img.shields.io/badge/Version-0.1.0-informational?style=flat-square) ![Type: application](https://img.shields.io/badge/Type-application-informational?style=flat-square) ![AppVersion: 1.0](https://img.shields.io/badge/AppVersion-1.0-informational?style=flat-square)

A Helm chart for deploying applications with StatefulSet and per-pod PVCs

## Values

| Key | Type | Default | Description |
|-----|------|---------|-------------|
| name | string | `"statefulset-app"` |  |
| replicaCount | int | `1` |  |
| image.repository | string | `"nginx"` |  |
| image.pullPolicy | string | `"IfNotPresent"` |  |
| image.tag | string | `"latest"` |  |
| imagePullSecrets | list | `[]` |  |
| nameOverride | string | `""` |  |
| fullnameOverride | string | `""` |  |
| serviceAccount.create | bool | `false` |  |
| serviceAccount.automount | bool | `false` |  |
| serviceAccount.annotations | object | `{}` |  |
| serviceAccount.name | string | `""` |  |
| podAnnotations | object | `{}` |  |
| podLabels | object | `{}` |  |
| podSecurityContext | object | `{}` |  |
| securityContext | object | `{}` |  |
| containerPort | int | `80` |  |
| service.enabled | bool | `true` |  |
| service.type | string | `"ClusterIP"` |  |
| service.port | int | `80` |  |
| service.annotations | object | `{}` |  |
| ingress.enabled | bool | `false` |  |
| ingress.className | string | `"nginx"` |  |
| ingress.annotations | object | `{}` |  |
| ingress.hosts[0].host | string | `"chart-example.local"` |  |
| ingress.hosts[0].paths[0].path | string | `"/"` |  |
| ingress.hosts[0].paths[0].pathType | string | `"Prefix"` |  |
| ingress.tls | list | `[]` |  |
| resources | object | `{}` |  |
| env | list | `[]` |  |
| envFrom | list | `[]` |  |
| livenessProbe | object | `{}` |  |
| readinessProbe | object | `{}` |  |
| volumeMounts | list | `[]` |  |
| volumes | list | `[]` |  |
| volumeClaimTemplates | list | `[]` |  |
| updateStrategy.type | string | `"RollingUpdate"` |  |
| updateStrategy.rollingUpdate.partition | int | `0` |  |
| podManagementPolicy | string | `"OrderedReady"` |  |
| serviceName | string | `""` |  |
| nodeSelector | object | `{}` |  |
| tolerations | list | `[]` |  |
| affinity | object | `{}` |  |

