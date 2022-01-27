# minio

![Version: 5.0.16](https://img.shields.io/badge/Version-5.0.16-informational?style=flat-square) ![AppVersion: master](https://img.shields.io/badge/AppVersion-master-informational?style=flat-square)

MinIO is a high performance data infrastructure for machine learning, analytics and application data workloads.

**Homepage:** <https://min.io>

## Maintainers

| Name | Email | Url |
| ---- | ------ | --- |
| Minio | dev@minio.io |  |
| Acaleph | hello@acale.ph |  |

## Source Code

* <https://github.com/minio/minio>

## Values

| Key | Type | Default | Description |
|-----|------|---------|-------------|
| DeploymentUpdate.maxSurge | string | `"100%"` |  |
| DeploymentUpdate.maxUnavailable | int | `0` |  |
| DeploymentUpdate.type | string | `"RollingUpdate"` |  |
| StatefulSetUpdate.updateStrategy | string | `"RollingUpdate"` |  |
| accessKey | string | `"AKIAIOSFODNN7EXAMPLE"` |  |
| affinity | object | `{}` |  |
| azuregateway.enabled | bool | `false` |  |
| azuregateway.replicas | int | `4` |  |
| b2gateway.enabled | bool | `false` |  |
| b2gateway.replicas | int | `4` |  |
| bucketRoot | string | `""` |  |
| buckets | list | `[]` |  |
| certsPath | string | `"/etc/minio/certs/"` |  |
| clusterDomain | string | `"cluster.local"` |  |
| configPathmc | string | `"/etc/minio/mc/"` |  |
| defaultBucket.enabled | bool | `false` |  |
| defaultBucket.name | string | `"bucket"` |  |
| defaultBucket.policy | string | `"none"` |  |
| defaultBucket.purge | bool | `false` |  |
| drivesPerNode | int | `1` |  |
| environment | string | `nil` |  |
| existingSecret | string | `""` |  |
| extraArgs | list | `[]` |  |
| fullnameOverride | string | `""` |  |
| gcsgateway.enabled | bool | `false` |  |
| gcsgateway.gcsKeyJson | string | `""` |  |
| gcsgateway.projectId | string | `""` |  |
| gcsgateway.replicas | int | `4` |  |
| image.pullPolicy | string | `"IfNotPresent"` |  |
| image.repository | string | `"minio/minio"` |  |
| image.tag | string | `"RELEASE.2020-03-06T22-23-56Z"` |  |
| ingress.annotations | object | `{}` |  |
| ingress.enabled | bool | `false` |  |
| ingress.hosts[0] | string | `"chart-example.local"` |  |
| ingress.labels | object | `{}` |  |
| ingress.path | string | `"/"` |  |
| ingress.tls | list | `[]` |  |
| livenessProbe.failureThreshold | int | `3` |  |
| livenessProbe.initialDelaySeconds | int | `5` |  |
| livenessProbe.periodSeconds | int | `30` |  |
| livenessProbe.successThreshold | int | `1` |  |
| livenessProbe.timeoutSeconds | int | `1` |  |
| makeBucketJob.annotations | string | `nil` |  |
| mcImage.pullPolicy | string | `"IfNotPresent"` |  |
| mcImage.repository | string | `"minio/mc"` |  |
| mcImage.tag | string | `"RELEASE.2020-03-06T23-29-45Z"` |  |
| metrics.serviceMonitor.additionalLabels | object | `{}` |  |
| metrics.serviceMonitor.enabled | bool | `false` |  |
| mode | string | `"standalone"` |  |
| mountPath | string | `"/export"` |  |
| nameOverride | string | `""` |  |
| nasgateway.enabled | bool | `false` |  |
| nasgateway.pv | string | `nil` |  |
| nasgateway.replicas | int | `4` |  |
| networkPolicy.allowExternal | bool | `true` |  |
| networkPolicy.enabled | bool | `false` |  |
| nodeSelector | object | `{}` |  |
| ossgateway.enabled | bool | `false` |  |
| ossgateway.endpointURL | string | `""` |  |
| ossgateway.replicas | int | `4` |  |
| persistence.VolumeName | string | `""` |  |
| persistence.accessMode | string | `"ReadWriteOnce"` |  |
| persistence.enabled | bool | `true` |  |
| persistence.existingClaim | string | `""` |  |
| persistence.size | string | `"10Gi"` |  |
| persistence.storageClass | string | `""` |  |
| persistence.subPath | string | `""` |  |
| podAnnotations | object | `{}` |  |
| podDisruptionBudget.enabled | bool | `false` |  |
| podDisruptionBudget.maxUnavailable | int | `1` |  |
| podLabels | object | `{}` |  |
| priorityClassName | string | `""` |  |
| readinessProbe.failureThreshold | int | `3` |  |
| readinessProbe.initialDelaySeconds | int | `60` |  |
| readinessProbe.periodSeconds | int | `15` |  |
| readinessProbe.successThreshold | int | `1` |  |
| readinessProbe.timeoutSeconds | int | `1` |  |
| replicas | int | `4` |  |
| resources.requests.cpu | string | `"250m"` |  |
| resources.requests.memory | string | `"256Mi"` |  |
| s3gateway.enabled | bool | `false` |  |
| s3gateway.replicas | int | `4` |  |
| s3gateway.serviceEndpoint | string | `""` |  |
| secretKey | string | `"wJalrXUtnFEMI/K7MDENG/bPxRfiCYEXAMPLEKEY"` |  |
| securityContext.enabled | bool | `false` |  |
| securityContext.fsGroup | int | `1000` |  |
| securityContext.runAsGroup | int | `1000` |  |
| securityContext.runAsUser | int | `1000` |  |
| service.annotations | object | `{}` |  |
| service.clusterIP | string | `nil` |  |
| service.externalIPs | list | `[]` |  |
| service.nodePort | int | `31311` |  |
| service.port | int | `9000` |  |
| service.type | string | `"ClusterIP"` |  |
| serviceAccount.create | bool | `true` |  |
| serviceAccount.name | string | `nil` |  |
| tls.certSecret | string | `""` |  |
| tls.enabled | bool | `false` |  |
| tls.privateKey | string | `"private.key"` |  |
| tls.publicCrt | string | `"public.crt"` |  |
| tolerations | list | `[]` |  |
| zones | int | `1` |  |

----------------------------------------------
Autogenerated from chart metadata using [helm-docs v1.5.0](https://github.com/norwoodj/helm-docs/releases/v1.5.0)
