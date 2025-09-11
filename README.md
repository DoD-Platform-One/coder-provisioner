<!-- Warning: Do not manually edit this file. See notes on gluon + helm-docs at the end of this file for more information. -->
# coder-provisioner

![Version: 2.24.3-bb.0](https://img.shields.io/badge/Version-2.24.3--bb.0-informational?style=flat-square) ![Type: application](https://img.shields.io/badge/Type-application-informational?style=flat-square) ![AppVersion: 2.24.3](https://img.shields.io/badge/AppVersion-2.24.3-informational?style=flat-square) ![Maintenance Track: community_maintained](https://img.shields.io/badge/Maintenance_Track-community_maintained-red?style=flat-square)

Remote development environments on your infrastructure

## Upstream References

- <https://github.com/coder/coder>
- <https://github.com/coder/coder/tree/main/helm/provisioner>

## Upstream Release Notes

- [Find upstream chart's release notes and CHANGELOG here](https://coder.com/docs/install/releases)

## Learn More

- [Application Overview](docs/overview.md)
- [Other Documentation](docs/)

## Pre-Requisites

- Kubernetes Cluster deployed
- Kubernetes config installed in `~/.kube/config`
- Helm installed

Kubernetes: `>= 1.19.0-0`

Install Helm

https://helm.sh/docs/intro/install/

## Deployment

- Clone down the repository
- cd into directory

```bash
helm install coder-provisioner chart/
```

## Values

| Key | Type | Default | Description |
|-----|------|---------|-------------|
| domain | string | `"bigbang.dev"` |  |
| monitoring.enabled | bool | `false` |  |
| monitoring.namespace | string | `"monitoring"` |  |
| upstream.nameOverride | string | `"coder-provisioner"` |  |
| upstream.coder.env | list | `[]` |  |
| upstream.coder.image.repo | string | `"registry1.dso.mil/ironbank/coder/coder-enterprise/coder-service-2"` |  |
| upstream.coder.image.tag | string | `"2.22.1"` |  |
| upstream.coder.image.pullPolicy | string | `"IfNotPresent"` |  |
| upstream.coder.image.pullSecrets[0].name | string | `"private-registry"` |  |
| upstream.coder.initContainers | list | `[]` |  |
| upstream.coder.annotations | object | `{}` |  |
| upstream.coder.labels | object | `{}` |  |
| upstream.coder.podAnnotations | object | `{}` |  |
| upstream.coder.podLabels | object | `{}` |  |
| upstream.coder.serviceAccount.workspacePerms | bool | `true` |  |
| upstream.coder.serviceAccount.enableDeployments | bool | `true` |  |
| upstream.coder.serviceAccount.annotations | object | `{}` |  |
| upstream.coder.serviceAccount.name | string | `"coder-provisioner"` |  |
| upstream.coder.serviceAccount.disableCreate | bool | `false` |  |
| upstream.coder.securityContext.runAsNonRoot | bool | `true` |  |
| upstream.coder.securityContext.runAsUser | int | `1000` |  |
| upstream.coder.securityContext.runAsGroup | int | `1000` |  |
| upstream.coder.securityContext.readOnlyRootFilesystem | string | `nil` |  |
| upstream.coder.securityContext.seccompProfile.type | string | `"RuntimeDefault"` |  |
| upstream.coder.securityContext.allowPrivilegeEscalation | bool | `false` |  |
| upstream.coder.volumes | list | `[]` |  |
| upstream.coder.volumeMounts | list | `[]` |  |
| upstream.coder.replicaCount | int | `1` |  |
| upstream.coder.lifecycle | object | `{}` |  |
| upstream.coder.resources | object | `{}` |  |
| upstream.coder.certs.secrets | list | `[]` |  |
| upstream.coder.affinity | object | `{}` |  |
| upstream.coder.tolerations | object | `{}` |  |
| upstream.coder.nodeSelector | object | `{}` |  |
| upstream.coder.command[0] | string | `"/opt/coder"` |  |
| upstream.coder.commandArgs | list | `[]` |  |
| upstream.provisionerDaemon.pskSecretName | string | `"coder-provisioner-psk"` |  |
| upstream.provisionerDaemon.keySecretName | string | `""` |  |
| upstream.provisionerDaemon.keySecretKey | string | `"key"` |  |
| upstream.provisionerDaemon.tags | object | `{}` |  |
| upstream.provisionerDaemon.terminationGracePeriodSeconds | int | `600` |  |
| upstream.extraTemplates | string | `nil` |  |

## Contributing

Please see the [contributing guide](./CONTRIBUTING.md) if you are interested in contributing.

---

_This file is programatically generated using `helm-docs` and some BigBang-specific templates. The `gluon` repository has [instructions for regenerating package READMEs](https://repo1.dso.mil/big-bang/product/packages/gluon/-/blob/master/docs/bb-package-readme.md)._

