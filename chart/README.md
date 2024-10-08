# sulfoxide-iron

![Version: 1.10.0](https://img.shields.io/badge/Version-1.10.0-informational?style=flat-square) ![Type: application](https://img.shields.io/badge/Type-application-informational?style=flat-square) ![AppVersion: 2.12.0](https://img.shields.io/badge/AppVersion-2.12.0-informational?style=flat-square)

Helm chart to deploy KEDA scaler as pod autoscaler

## Requirements

| Repository | Name | Version |
|------------|------|---------|
| https://kedacore.github.io/charts | keda | 2.15.0 |

## Values

| Key | Type | Default | Description |
|-----|------|---------|-------------|
| keda | object | `{"additionalAnnotations":{"<<":{"atomi.cloud/layer":"1","atomi.cloud/platform":"sulfoxide","atomi.cloud/service":"iron"}},"additionalLabels":{"<<":{"atomi.cloud/layer":"1","atomi.cloud/platform":"sulfoxide","atomi.cloud/service":"iron"}},"podAnnotations":{"keda":{"<<":{"atomi.cloud/layer":"1","atomi.cloud/platform":"sulfoxide","atomi.cloud/service":"iron"},"atomi.cloud/module":"operator"},"metricsAdapter":{"<<":{"atomi.cloud/layer":"1","atomi.cloud/platform":"sulfoxide","atomi.cloud/service":"iron"},"atomi.cloud/module":"metrics-adapter"},"webhooks":{"<<":{"atomi.cloud/layer":"1","atomi.cloud/platform":"sulfoxide","atomi.cloud/service":"iron"},"atomi.cloud/module":"webhooks"}},"podLabels":{"keda":{"<<":{"atomi.cloud/layer":"1","atomi.cloud/platform":"sulfoxide","atomi.cloud/service":"iron"},"atomi.cloud/module":"operator"},"metricsAdapter":{"<<":{"atomi.cloud/layer":"1","atomi.cloud/platform":"sulfoxide","atomi.cloud/service":"iron"},"atomi.cloud/module":"metrics-adapter"},"webhooks":{"<<":{"atomi.cloud/layer":"1","atomi.cloud/platform":"sulfoxide","atomi.cloud/service":"iron"},"atomi.cloud/module":"webhooks"}},"podSecurityContext":{"<<":{"fsGroup":1000,"runAsGroup":1000,"runAsNonRoot":true,"runAsUser":1000}},"prometheus":{"metricServer":{"enabled":true,"serviceMonitor":{"enabled":true}},"operator":{"enabled":true,"serviceMonitor":{"enabled":true}},"webhooks":{"enabled":true,"serviceMonitor":{"enabled":true}}},"securityContext":{"<<":{"allowPrivilegeEscalation":false,"capabilities":{"drop":["ALL"]},"readOnlyRootFilesystem":true,"runAsGroup":1000,"runAsNonRoot":true,"runAsUser":1000}},"topologySpreadConstraints":{"metricsServer":[{"labelSelector":{"matchLabels":{"<<":{"atomi.cloud/layer":"1","atomi.cloud/platform":"sulfoxide","atomi.cloud/service":"iron"},"atomi.cloud/module":"metrics-adapter"}},"maxSkew":1,"topologyKey":"topology.kubernetes.io/zone","whenUnsatisfiable":"ScheduleAnyway"}],"operator":[{"labelSelector":{"matchLabels":{"<<":{"atomi.cloud/layer":"1","atomi.cloud/platform":"sulfoxide","atomi.cloud/service":"iron"},"atomi.cloud/module":"operator"}},"maxSkew":1,"topologyKey":"topology.kubernetes.io/zone","whenUnsatisfiable":"ScheduleAnyway"}],"webhooks":[{"labelSelector":{"matchLabels":{"<<":{"atomi.cloud/layer":"1","atomi.cloud/platform":"sulfoxide","atomi.cloud/service":"iron"},"atomi.cloud/module":"webhooks"}},"maxSkew":1,"topologyKey":"topology.kubernetes.io/zone","whenUnsatisfiable":"ScheduleAnyway"}]}}` | KEDA Configuration. See [Helm Config for KEDA](https://github.com/kedacore/charts/tree/main/keda). |
| podSecurityContext | object | `{"fsGroup":1000,"runAsGroup":1000,"runAsNonRoot":true,"runAsUser":1000}` | YAML Anchor for PodSecurityContext |
| securityContext | object | `{"allowPrivilegeEscalation":false,"capabilities":{"drop":["ALL"]},"readOnlyRootFilesystem":true,"runAsGroup":1000,"runAsNonRoot":true,"runAsUser":1000}` | YAML Anchor for SecurityContext |
| tags | object | `{"atomi.cloud/layer":"1","atomi.cloud/platform":"sulfoxide","atomi.cloud/service":"iron"}` | Kubernetes labels and annotations, following Service Tree |

----------------------------------------------
Autogenerated from chart metadata using [helm-docs v1.14.2](https://github.com/norwoodj/helm-docs/releases/v1.14.2)
