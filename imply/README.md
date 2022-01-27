# imply

![Version: 2021.05-1](https://img.shields.io/badge/Version-2021.05--1-informational?style=flat-square) ![AppVersion: 2021.05-1](https://img.shields.io/badge/AppVersion-2021.05--1-informational?style=flat-square)

Imply Manager

**Homepage:** <https://imply.io>

## Maintainers

| Name | Email | Url |
| ---- | ------ | --- |
| Imply | contact@imply.io |  |

## Requirements

| Repository | Name | Version |
|------------|------|---------|
| https://kubernetes-charts-incubator.storage.googleapis.com/ | zookeeper | 2.1.1 |
| https://kubernetes-charts.storage.googleapis.com/ | minio | 5.0.16 |
| https://kubernetes-charts.storage.googleapis.com/ | mysql | 1.5.0 |

## Values

| Key | Type | Default | Description |
|-----|------|---------|-------------|
| agents.clusterName | string | `"default"` |  |
| agents.managerHost | string | `"{{ include \"imply.manager.internalService.fullname\" . }}"` |  |
| agents.terminationGracePeriodSeconds | int | `86400` |  |
| dataTier1.affinity | object | `{}` |  |
| dataTier1.annotations | object | `{}` |  |
| dataTier1.extraEnv | list | `[]` |  |
| dataTier1.extraVolumeClaimTemplates | object | `{}` |  |
| dataTier1.extraVolumeMounts | list | `[]` |  |
| dataTier1.extraVolumes | list | `[]` |  |
| dataTier1.labels | object | `{}` |  |
| dataTier1.nodeSelector | object | `{}` |  |
| dataTier1.persistence.enabled | bool | `true` |  |
| dataTier1.podDisruptionBudget.maxUnavailable | int | `1` |  |
| dataTier1.replicaCount | int | `2` |  |
| dataTier1.resources.requests.cpu | string | `"400m"` |  |
| dataTier1.resources.requests.memory | string | `"1300M"` |  |
| dataTier1.schedulerName | string | `""` |  |
| dataTier1.segmentCacheVolume.resources.requests.storage | string | `"20Gi"` |  |
| dataTier1.segmentCacheVolume.selector | object | `{}` |  |
| dataTier1.segmentCacheVolume.storageClassName | string | `nil` |  |
| dataTier1.serviceAccountName | string | `""` |  |
| dataTier1.sysctlInitContainer.enabled | bool | `true` |  |
| dataTier1.sysctlInitContainer.sysctlKernelThreadsMax | int | `999999` |  |
| dataTier1.sysctlInitContainer.sysctlVmMaxMapCount | int | `500000` |  |
| dataTier1.tmpVolume.resources.requests.storage | string | `"10Gi"` |  |
| dataTier1.tmpVolume.selector | object | `{}` |  |
| dataTier1.tmpVolume.storageClassName | string | `nil` |  |
| dataTier1.tolerations | list | `[]` |  |
| dataTier2.affinity | object | `{}` |  |
| dataTier2.annotations | object | `{}` |  |
| dataTier2.extraEnv | list | `[]` |  |
| dataTier2.extraVolumeClaimTemplates | object | `{}` |  |
| dataTier2.extraVolumeMounts | list | `[]` |  |
| dataTier2.extraVolumes | list | `[]` |  |
| dataTier2.labels | object | `{}` |  |
| dataTier2.nodeSelector | object | `{}` |  |
| dataTier2.persistence.enabled | bool | `true` |  |
| dataTier2.podDisruptionBudget.maxUnavailable | int | `1` |  |
| dataTier2.replicaCount | int | `0` |  |
| dataTier2.resources.requests.cpu | string | `"400m"` |  |
| dataTier2.resources.requests.memory | string | `"1300M"` |  |
| dataTier2.schedulerName | string | `""` |  |
| dataTier2.segmentCacheVolume.resources.requests.storage | string | `"20Gi"` |  |
| dataTier2.segmentCacheVolume.selector | object | `{}` |  |
| dataTier2.segmentCacheVolume.storageClassName | string | `nil` |  |
| dataTier2.serviceAccountName | string | `""` |  |
| dataTier2.sysctlInitContainer.enabled | bool | `true` |  |
| dataTier2.sysctlInitContainer.sysctlKernelThreadsMax | int | `999999` |  |
| dataTier2.sysctlInitContainer.sysctlVmMaxMapCount | int | `500000` |  |
| dataTier2.tmpVolume.resources.requests.storage | string | `"10Gi"` |  |
| dataTier2.tmpVolume.selector | object | `{}` |  |
| dataTier2.tmpVolume.storageClassName | string | `nil` |  |
| dataTier2.tolerations | list | `[]` |  |
| dataTier3.affinity | object | `{}` |  |
| dataTier3.annotations | object | `{}` |  |
| dataTier3.extraEnv | list | `[]` |  |
| dataTier3.extraVolumeClaimTemplates | object | `{}` |  |
| dataTier3.extraVolumeMounts | list | `[]` |  |
| dataTier3.extraVolumes | list | `[]` |  |
| dataTier3.labels | object | `{}` |  |
| dataTier3.nodeSelector | object | `{}` |  |
| dataTier3.persistence.enabled | bool | `true` |  |
| dataTier3.podDisruptionBudget.maxUnavailable | int | `1` |  |
| dataTier3.replicaCount | int | `0` |  |
| dataTier3.resources.requests.cpu | string | `"400m"` |  |
| dataTier3.resources.requests.memory | string | `"1300M"` |  |
| dataTier3.schedulerName | string | `""` |  |
| dataTier3.segmentCacheVolume.resources.requests.storage | string | `"20Gi"` |  |
| dataTier3.segmentCacheVolume.selector | object | `{}` |  |
| dataTier3.segmentCacheVolume.storageClassName | string | `nil` |  |
| dataTier3.serviceAccountName | string | `""` |  |
| dataTier3.sysctlInitContainer.enabled | bool | `true` |  |
| dataTier3.sysctlInitContainer.sysctlKernelThreadsMax | int | `999999` |  |
| dataTier3.sysctlInitContainer.sysctlVmMaxMapCount | int | `500000` |  |
| dataTier3.tmpVolume.resources.requests.storage | string | `"10Gi"` |  |
| dataTier3.tmpVolume.selector | object | `{}` |  |
| dataTier3.tmpVolume.storageClassName | string | `nil` |  |
| dataTier3.tolerations | list | `[]` |  |
| deployments.agents | bool | `true` |  |
| deployments.manager | bool | `true` |  |
| deployments.minio | bool | `true` |  |
| deployments.mysql | bool | `true` |  |
| deployments.zookeeper | bool | `true` |  |
| druid.brokerRuntimeProperties | list | `[]` |  |
| druid.commonRuntimeProperties[0] | string | `"# MinIO configurations"` |  |
| druid.commonRuntimeProperties[1] | string | `"druid.s3.endpoint.url=http://{{ .Release.Name }}-minio:9000"` |  |
| druid.commonRuntimeProperties[2] | string | `"druid.s3.enablePathStyleAccess=true"` |  |
| druid.coordinatorRuntimeProperties | list | `[]` |  |
| druid.deepStorage.password | string | `"implypassword"` |  |
| druid.deepStorage.path | string | `"s3://imply/"` |  |
| druid.deepStorage.type | string | `"s3"` |  |
| druid.deepStorage.user | string | `"imply"` |  |
| druid.historicalRuntimeProperties | list | `[]` |  |
| druid.historicalTier1RuntimeProperties | list | `[]` |  |
| druid.historicalTier2RuntimeProperties | list | `[]` |  |
| druid.historicalTier3RuntimeProperties | list | `[]` |  |
| druid.implyVersion | string | `""` |  |
| druid.metadataStore.host | string | `"{{ .Release.Name }}-mysql"` |  |
| druid.metadataStore.password | string | `"imply"` |  |
| druid.metadataStore.port | int | `3306` |  |
| druid.metadataStore.type | string | `"mysql"` |  |
| druid.metadataStore.user | string | `"root"` |  |
| druid.middleManagerRuntimeProperties | list | `[]` |  |
| druid.middleManagerTier1RuntimeProperties | list | `[]` |  |
| druid.middleManagerTier2RuntimeProperties | list | `[]` |  |
| druid.middleManagerTier3RuntimeProperties | list | `[]` |  |
| druid.overlordRuntimeProperties | list | `[]` |  |
| druid.pivotRuntimeProperties | list | `[]` |  |
| druid.routerRuntimeProperties | list | `[]` |  |
| druid.update | string | `"disabled"` |  |
| druid.zk.basePath | string | `"imply"` |  |
| druid.zk.connectString | string | `"{{ .Release.Name }}-zookeeper:2181"` |  |
| fullnameOverride | string | `nil` |  |
| images.agent.repository | string | `"imply/agent"` |  |
| images.agent.tag | string | `"v2"` |  |
| images.manager.repository | string | `"imply/manager"` |  |
| images.manager.tag | string | `"2021.05"` |  |
| images.pullPolicy | string | `"IfNotPresent"` |  |
| manager.affinity | object | `{}` |  |
| manager.annotations | object | `{}` |  |
| manager.customVersions | list | `[]` |  |
| manager.extraEnv | list | `[]` |  |
| manager.extraInitContainers | list | `[]` |  |
| manager.extraVolumeMounts | list | `[]` |  |
| manager.extraVolumes | list | `[]` |  |
| manager.ingress.annotations | object | `{}` |  |
| manager.ingress.enabled | bool | `false` |  |
| manager.ingress.paths[0] | string | `"/*"` |  |
| manager.ingress.tls | object | `{}` |  |
| manager.labels | object | `{}` |  |
| manager.licenseKey | string | `""` |  |
| manager.metadataStore.database | string | `"imply-manager"` |  |
| manager.metadataStore.host | string | `"{{ .Release.Name }}-mysql"` |  |
| manager.metadataStore.password | string | `"imply"` |  |
| manager.metadataStore.port | int | `3306` |  |
| manager.metadataStore.type | string | `"mysql"` |  |
| manager.metadataStore.user | string | `"root"` |  |
| manager.nodeSelector | object | `{}` |  |
| manager.resources.requests.cpu | string | `"300m"` |  |
| manager.resources.requests.memory | string | `"500M"` |  |
| manager.schedulerName | string | `""` |  |
| manager.secretName | string | `"imply-secrets"` |  |
| manager.service.annotations | object | `{}` |  |
| manager.service.enabled | bool | `false` |  |
| manager.service.labels | object | `{}` |  |
| manager.service.port | string | `"{{ ternary 80 443 (empty .Values.security.tls) }}"` |  |
| manager.service.protocol | string | `"TCP"` |  |
| manager.service.type | string | `"LoadBalancer"` |  |
| manager.serviceAccountName | string | `""` |  |
| manager.tolerations | list | `[]` |  |
| master.affinity | object | `{}` |  |
| master.annotations | object | `{}` |  |
| master.extraEnv | list | `[]` |  |
| master.extraVolumeMounts | list | `[]` |  |
| master.extraVolumes | list | `[]` |  |
| master.labels | object | `{}` |  |
| master.nodeSelector | object | `{}` |  |
| master.podDisruptionBudget.maxUnavailable | int | `1` |  |
| master.replicaCount | int | `1` |  |
| master.resources.requests.cpu | string | `"200m"` |  |
| master.resources.requests.memory | string | `"500M"` |  |
| master.schedulerName | string | `""` |  |
| master.serviceAccountName | string | `""` |  |
| master.tolerations | list | `[]` |  |
| minio.accessKey | string | `"imply"` |  |
| minio.defaultBucket.enabled | bool | `true` |  |
| minio.defaultBucket.name | string | `"imply"` |  |
| minio.persistence.enabled | bool | `true` |  |
| minio.persistence.size | string | `"10Gi"` |  |
| minio.resources.requests.cpu | string | `"100m"` |  |
| minio.resources.requests.memory | string | `"256Mi"` |  |
| minio.secretKey | string | `"implypassword"` |  |
| mysql.mysqlRootPassword | string | `"imply"` |  |
| mysql.persistence.enabled | bool | `true` |  |
| nameOverride | string | `nil` |  |
| query.affinity | object | `{}` |  |
| query.annotations | object | `{}` |  |
| query.extraEnv | list | `[]` |  |
| query.extraVolumeMounts | list | `[]` |  |
| query.extraVolumes | list | `[]` |  |
| query.ingress.pivot.annotations | object | `{}` |  |
| query.ingress.pivot.enabled | bool | `false` |  |
| query.ingress.pivot.host | string | `nil` |  |
| query.ingress.pivot.paths[0] | string | `"/*"` |  |
| query.ingress.pivot.tls | object | `{}` |  |
| query.ingress.router.annotations | object | `{}` |  |
| query.ingress.router.enabled | bool | `false` |  |
| query.ingress.router.host | string | `nil` |  |
| query.ingress.router.paths[0] | string | `"/*"` |  |
| query.ingress.router.tls | object | `{}` |  |
| query.labels | object | `{}` |  |
| query.nodeSelector | object | `{}` |  |
| query.podDisruptionBudget.maxUnavailable | int | `1` |  |
| query.replicaCount | int | `1` |  |
| query.resources.requests.cpu | string | `"400m"` |  |
| query.resources.requests.memory | string | `"1200M"` |  |
| query.schedulerName | string | `""` |  |
| query.service.annotations | object | `{}` |  |
| query.service.labels | object | `{}` |  |
| query.service.pivotPort | int | `9095` |  |
| query.service.protocol | string | `"TCP"` |  |
| query.service.routerPort | int | `8888` |  |
| query.service.type | string | `"ClusterIP"` |  |
| query.serviceAccountName | string | `""` |  |
| query.tolerations | list | `[]` |  |
| security | object | `{}` |  |
| zookeeper.env.ZK_HEAP_SIZE | string | `"512M"` |  |
| zookeeper.env.ZK_PURGE_INTERVAL | int | `1` |  |
| zookeeper.env.ZOO_AUTOPURGE_PURGEINTERVAL | int | `1` |  |
| zookeeper.persistence.enabled | bool | `true` |  |
| zookeeper.persistence.size | string | `"10Gi"` |  |
| zookeeper.replicaCount | int | `1` |  |

----------------------------------------------
Autogenerated from chart metadata using [helm-docs v1.5.0](https://github.com/norwoodj/helm-docs/releases/v1.5.0)
