# Changelog

## 2.0.0 (2026-10-21)


### ⚠ BREAKING CHANGES

* the package version no longer embeds the upstream version: the tag is `2.0.0`, the upstream version is `appVersion` in the descriptor
* the parameters are a closed JSON Schema: an unknown parameter is refused
* the role `dataviz` is renamed `okdp.io/bi`; the dependencies are `okdp.io/ingress`, `okdp.io/certificate-manager`, `okdp.io/identity-provider`, `okdp.io/platform-tools` and `okdp.io/secrets-backend`, the databases and the Trino instances are connections
* `metadataDb`, `examplesDb` and `datasources[].trino` are plain strings naming Connections, read through `inputs` entries
* `oidcRoleMapping` is replaced by `access`, the groups granted each Superset role
* `oidc.clientProvisioning` defaults to `dcr`: the package registers its OAuth client unless the platform Context says `existing`

### Features

* describe the package with contract 0.2
* register the login client and the Trino client through dynamic client registration when the platform provisions clients that way
* Apache Superset 6.1.0

## [1.1.0](https://github.com/OKDP/platform-packages/compare/superset/v1.0.0...superset/v1.1.0) (2026-09-25)


### Features

* **superset:** add a chart locale parameter ([082e702](https://github.com/OKDP/platform-packages/commit/082e702722bcc395a2930bbd46f732c4486041c4))


### Bug Fixes

* replace release please anotation with custom release increment ([99c6bdc](https://github.com/OKDP/platform-packages/commit/99c6bdc8b8158dea5fcb1a49107529d35808cdb9))
