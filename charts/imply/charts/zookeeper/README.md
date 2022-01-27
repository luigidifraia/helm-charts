# zookeeper

![Version: 2.1.1](https://img.shields.io/badge/Version-2.1.1-informational?style=flat-square) ![AppVersion: 3.5.5](https://img.shields.io/badge/AppVersion-3.5.5-informational?style=flat-square)

Centralized service for maintaining configuration information, naming, providing distributed synchronization, and providing group services.

**Homepage:** <https://zookeeper.apache.org/>

## Maintainers

| Name | Email | Url |
| ---- | ------ | --- |
| lachie83 | lachlan.evenson@microsoft.com |  |
| kow3ns | owensk@google.com |  |

## Source Code

* <https://github.com/apache/zookeeper>
* <https://github.com/kubernetes/contrib/tree/master/statefulsets/zookeeper>

## Requirements

Kubernetes: `^1.10.0-0`

## Values

| Key | Type | Default | Description |
|-----|------|---------|-------------|
| affinity | object | `{}` |  |
| command[0] | string | `"/bin/bash"` |  |
| command[1] | string | `"-xec"` |  |
| command[2] | string | `"/config-scripts/run"` |  |
| env.JMXAUTH | string | `"false"` |  |
| env.JMXDISABLE | string | `"false"` |  |
| env.JMXPORT | int | `1099` |  |
| env.JMXSSL | string | `"false"` |  |
| env.ZK_SYNC_LIMIT | int | `10` |  |
| env.ZK_TICK_TIME | int | `2000` |  |
| env.ZOO_AUTOPURGE_PURGEINTERVAL | int | `0` |  |
| env.ZOO_AUTOPURGE_SNAPRETAINCOUNT | int | `3` |  |
| env.ZOO_INIT_LIMIT | int | `5` |  |
| env.ZOO_MAX_CLIENT_CNXNS | int | `60` |  |
| env.ZOO_PORT | int | `2181` |  |
| env.ZOO_STANDALONE_ENABLED | bool | `false` |  |
| env.ZOO_TICK_TIME | int | `2000` |  |
| exporters.jmx.config.lowercaseOutputName | bool | `false` |  |
| exporters.jmx.config.rules[0].name | string | `"zookeeper_$2"` |  |
| exporters.jmx.config.rules[0].pattern | string | `"org.apache.ZooKeeperService<name0=ReplicatedServer_id(\\d+)><>(\\w+)"` |  |
| exporters.jmx.config.rules[1].labels.replicaId | string | `"$2"` |  |
| exporters.jmx.config.rules[1].name | string | `"zookeeper_$3"` |  |
| exporters.jmx.config.rules[1].pattern | string | `"org.apache.ZooKeeperService<name0=ReplicatedServer_id(\\d+), name1=replica.(\\d+)><>(\\w+)"` |  |
| exporters.jmx.config.rules[2].labels.memberType | string | `"$3"` |  |
| exporters.jmx.config.rules[2].labels.replicaId | string | `"$2"` |  |
| exporters.jmx.config.rules[2].name | string | `"zookeeper_$4"` |  |
| exporters.jmx.config.rules[2].pattern | string | `"org.apache.ZooKeeperService<name0=ReplicatedServer_id(\\d+), name1=replica.(\\d+), name2=(\\w+)><>(\\w+)"` |  |
| exporters.jmx.config.rules[3].labels.memberType | string | `"$3"` |  |
| exporters.jmx.config.rules[3].labels.replicaId | string | `"$2"` |  |
| exporters.jmx.config.rules[3].name | string | `"zookeeper_$4_$5"` |  |
| exporters.jmx.config.rules[3].pattern | string | `"org.apache.ZooKeeperService<name0=ReplicatedServer_id(\\d+), name1=replica.(\\d+), name2=(\\w+), name3=(\\w+)><>(\\w+)"` |  |
| exporters.jmx.config.startDelaySeconds | int | `30` |  |
| exporters.jmx.enabled | bool | `false` |  |
| exporters.jmx.env | object | `{}` |  |
| exporters.jmx.image.pullPolicy | string | `"IfNotPresent"` |  |
| exporters.jmx.image.repository | string | `"sscaling/jmx-prometheus-exporter"` |  |
| exporters.jmx.image.tag | string | `"0.3.0"` |  |
| exporters.jmx.livenessProbe.failureThreshold | int | `8` |  |
| exporters.jmx.livenessProbe.httpGet.path | string | `"/metrics"` |  |
| exporters.jmx.livenessProbe.httpGet.port | string | `"jmxxp"` |  |
| exporters.jmx.livenessProbe.initialDelaySeconds | int | `30` |  |
| exporters.jmx.livenessProbe.periodSeconds | int | `15` |  |
| exporters.jmx.livenessProbe.successThreshold | int | `1` |  |
| exporters.jmx.livenessProbe.timeoutSeconds | int | `60` |  |
| exporters.jmx.path | string | `"/metrics"` |  |
| exporters.jmx.ports.jmxxp.containerPort | int | `9404` |  |
| exporters.jmx.ports.jmxxp.protocol | string | `"TCP"` |  |
| exporters.jmx.readinessProbe.failureThreshold | int | `8` |  |
| exporters.jmx.readinessProbe.httpGet.path | string | `"/metrics"` |  |
| exporters.jmx.readinessProbe.httpGet.port | string | `"jmxxp"` |  |
| exporters.jmx.readinessProbe.initialDelaySeconds | int | `30` |  |
| exporters.jmx.readinessProbe.periodSeconds | int | `15` |  |
| exporters.jmx.readinessProbe.successThreshold | int | `1` |  |
| exporters.jmx.readinessProbe.timeoutSeconds | int | `60` |  |
| exporters.jmx.resources | object | `{}` |  |
| exporters.jmx.serviceMonitor.interval | string | `"30s"` |  |
| exporters.jmx.serviceMonitor.scheme | string | `"http"` |  |
| exporters.jmx.serviceMonitor.scrapeTimeout | string | `"30s"` |  |
| exporters.zookeeper.config.logLevel | string | `"info"` |  |
| exporters.zookeeper.config.resetOnScrape | string | `"true"` |  |
| exporters.zookeeper.enabled | bool | `false` |  |
| exporters.zookeeper.env | object | `{}` |  |
| exporters.zookeeper.image.pullPolicy | string | `"IfNotPresent"` |  |
| exporters.zookeeper.image.repository | string | `"josdotso/zookeeper-exporter"` |  |
| exporters.zookeeper.image.tag | string | `"v1.1.2"` |  |
| exporters.zookeeper.livenessProbe.failureThreshold | int | `8` |  |
| exporters.zookeeper.livenessProbe.httpGet.path | string | `"/metrics"` |  |
| exporters.zookeeper.livenessProbe.httpGet.port | string | `"zookeeperxp"` |  |
| exporters.zookeeper.livenessProbe.initialDelaySeconds | int | `30` |  |
| exporters.zookeeper.livenessProbe.periodSeconds | int | `15` |  |
| exporters.zookeeper.livenessProbe.successThreshold | int | `1` |  |
| exporters.zookeeper.livenessProbe.timeoutSeconds | int | `60` |  |
| exporters.zookeeper.path | string | `"/metrics"` |  |
| exporters.zookeeper.ports.zookeeperxp.containerPort | int | `9141` |  |
| exporters.zookeeper.ports.zookeeperxp.protocol | string | `"TCP"` |  |
| exporters.zookeeper.readinessProbe.failureThreshold | int | `8` |  |
| exporters.zookeeper.readinessProbe.httpGet.path | string | `"/metrics"` |  |
| exporters.zookeeper.readinessProbe.httpGet.port | string | `"zookeeperxp"` |  |
| exporters.zookeeper.readinessProbe.initialDelaySeconds | int | `30` |  |
| exporters.zookeeper.readinessProbe.periodSeconds | int | `15` |  |
| exporters.zookeeper.readinessProbe.successThreshold | int | `1` |  |
| exporters.zookeeper.readinessProbe.timeoutSeconds | int | `60` |  |
| exporters.zookeeper.resources | object | `{}` |  |
| exporters.zookeeper.serviceMonitor.interval | string | `"30s"` |  |
| exporters.zookeeper.serviceMonitor.scheme | string | `"http"` |  |
| exporters.zookeeper.serviceMonitor.scrapeTimeout | string | `"30s"` |  |
| headless.annotations | object | `{}` |  |
| image.pullPolicy | string | `"IfNotPresent"` |  |
| image.repository | string | `"zookeeper"` |  |
| image.tag | string | `"3.5.5"` |  |
| jobs.chroots.activeDeadlineSeconds | int | `300` |  |
| jobs.chroots.backoffLimit | int | `5` |  |
| jobs.chroots.completions | int | `1` |  |
| jobs.chroots.config.create | list | `[]` |  |
| jobs.chroots.enabled | bool | `false` |  |
| jobs.chroots.env | list | `[]` |  |
| jobs.chroots.parallelism | int | `1` |  |
| jobs.chroots.resources | object | `{}` |  |
| jobs.chroots.restartPolicy | string | `"Never"` |  |
| nodeSelector | object | `{}` |  |
| persistence.accessMode | string | `"ReadWriteOnce"` |  |
| persistence.enabled | bool | `true` |  |
| persistence.size | string | `"5Gi"` |  |
| podAnnotations | object | `{}` |  |
| podDisruptionBudget.maxUnavailable | int | `1` |  |
| podLabels | object | `{}` |  |
| ports.client.containerPort | int | `2181` |  |
| ports.client.protocol | string | `"TCP"` |  |
| ports.election.containerPort | int | `3888` |  |
| ports.election.protocol | string | `"TCP"` |  |
| ports.server.containerPort | int | `2888` |  |
| ports.server.protocol | string | `"TCP"` |  |
| priorityClassName | string | `""` |  |
| prometheus.serviceMonitor.enabled | bool | `false` |  |
| prometheus.serviceMonitor.selector | object | `{}` |  |
| replicaCount | int | `3` |  |
| resources | object | `{}` |  |
| securityContext.fsGroup | int | `1000` |  |
| securityContext.runAsUser | int | `1000` |  |
| service.annotations | object | `{}` |  |
| service.ports.client.port | int | `2181` |  |
| service.ports.client.protocol | string | `"TCP"` |  |
| service.ports.client.targetPort | string | `"client"` |  |
| service.type | string | `"ClusterIP"` |  |
| terminationGracePeriodSeconds | int | `1800` |  |
| tolerations | list | `[]` |  |
| updateStrategy.type | string | `"RollingUpdate"` |  |

----------------------------------------------
Autogenerated from chart metadata using [helm-docs v1.5.0](https://github.com/norwoodj/helm-docs/releases/v1.5.0)
