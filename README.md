# istio-operator

![Version: 1.21.2-bb.0](https://img.shields.io/badge/Version-1.21.2--bb.0-informational?style=flat-square) ![AppVersion: 1.21.2](https://img.shields.io/badge/AppVersion-1.21.2-informational?style=flat-square)

Helm chart for deploying Istio operator

## Upstream References

* <https://github.com/istio/istio/tree/master/operator>

## Learn More
* [Application Overview](docs/overview.md)
* [Other Documentation](docs/)

## Pre-Requisites

* Kubernetes Cluster deployed
* Kubernetes config installed in `~/.kube/config`
* Helm installed

Install Helm

https://helm.sh/docs/intro/install/

## Deployment

* Clone down the repository
* cd into directory
```bash
helm install istio-operator chart/
```

## Values

| Key | Type | Default | Description |
|-----|------|---------|-------------|
| defaults.hub | string | `"registry1.dso.mil/ironbank/opensource/istio"` |  |
| defaults.image | string | `"operator"` |  |
| defaults.tag | string | `"1.21.2"` |  |
| defaults.imagePullSecrets | list | `[]` |  |
| defaults.imagePullPolicy | string | `""` |  |
| defaults.watchedNamespaces | string | `"istio-system"` |  |
| defaults.waitForResourcesTimeout | string | `"300s"` |  |
| defaults.enableCRDTemplates | bool | `false` |  |
| defaults.revision | string | `""` |  |
| defaults.deploymentHistory | int | `10` |  |
| defaults.operator.monitoring.host | string | `"0.0.0.0"` |  |
| defaults.operator.monitoring.port | int | `8383` |  |
| defaults.operator.resources.limits.cpu | string | `"200m"` |  |
| defaults.operator.resources.limits.memory | string | `"256Mi"` |  |
| defaults.operator.resources.requests.cpu | string | `"200m"` |  |
| defaults.operator.resources.requests.memory | string | `"256Mi"` |  |
| defaults.operator.seccompProfile | object | `{}` |  |
| defaults.nodeSelector | object | `{}` |  |
| defaults.tolerations | list | `[]` |  |
| defaults.affinity | object | `{}` |  |
| defaults.podLabels | object | `{}` |  |
| defaults.podAnnotations | object | `{}` |  |
| createNamespace | bool | `true` |  |
| operatorNamespace | string | `"istio-operator"` |  |
| enterprise | bool | `false` | Tetrate Istio Distribution - Tetrate provides FIPs verified Istio and Envoy software and support, validated through the FIPs Boring Crypto module. Find out more from Tetrate - https://www.tetrate.io/tetrate-istio-subscription |
| tidHub | string | `"registry1.dso.mil/ironbank/tetrate/istio"` |  |
| tidTag | string | `"1.21.2-tetratefips-v0"` |  |
| monitoring.enabled | bool | `false` |  |
| networkPolicies.enabled | bool | `false` |  |
| networkPolicies.controlPlaneCidr | string | `"0.0.0.0/0"` |  |
| networkPolicies.additionalPolicies | list | `[]` |  |

## Contributing

Please see the [contributing guide](./CONTRIBUTING.md) if you are interested in contributing.
