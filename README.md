<!-- Warning: Do not manually edit this file. See notes on gluon + helm-docs at the end of this file for more information. -->
# coder-provisioner

![Version: 2.22.1-bb.0](https://img.shields.io/badge/Version-2.22.1--bb.0-informational?style=flat-square) ![Type: application](https://img.shields.io/badge/Type-application-informational?style=flat-square) ![AppVersion: 2.22.1](https://img.shields.io/badge/AppVersion-2.22.1-informational?style=flat-square) ![Maintenance Track: community_maintained](https://img.shields.io/badge/Maintenance_Track-community_maintained-red?style=flat-square)

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
| upstream.coder.image.repo | string | `"registry1.dso.mil/ironbank/coder/coder-enterprise/coder-service-2"` |  |
| upstream.coder.image.tag | string | `"2.22.1"` |  |
| upstream.coder.image.pullPolicy | string | `"IfNotPresent"` |  |
| upstream.coder.image.pullSecrets[0].name | string | `"private-registry"` |  |

## Contributing

Please see the [contributing guide](./CONTRIBUTING.md) if you are interested in contributing.

---

_This file is programatically generated using `helm-docs` and some BigBang-specific templates. The `gluon` repository has [instructions for regenerating package READMEs](https://repo1.dso.mil/big-bang/product/packages/gluon/-/blob/master/docs/bb-package-readme.md)._

