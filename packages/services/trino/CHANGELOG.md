# Changelog

## 2.0.0 (2026-10-21)


### ⚠ BREAKING CHANGES

* the package version no longer embeds the upstream version: the tag is `2.0.0`, the upstream version is `appVersion` in the descriptor
* the parameters are a closed JSON Schema: an unknown parameter is refused
* the role `interactive-query` is renamed `okdp.io/sql-query`; the dependency on `data-catalog` is dropped, the catalogs are connections; the dependencies are `okdp.io/ingress`, `okdp.io/certificate-manager`, `okdp.io/identity-provider`, `okdp.io/platform-tools` and `okdp.io/secrets-backend`
* `hiveCatalogs[].metastore`, `hiveCatalogs[].storage`, `icebergCatalogs[].catalog` and `icebergCatalogs[].storage` are plain strings naming Connections, read through `inputs` entries, one per item
* `icebergCatalogs[].oidcSecretRef` is required: the Polaris principal is never the Trino OIDC client; catalog names match `^[a-z][a-z0-9_-]*$`
* `enableOPAL` needs `enableOPA`
* `oidc.clientProvisioning` defaults to `dcr`: the package registers its OAuth client unless the platform Context says `existing`

### Features

* describe the package with contract 0.2
* Trino 484, chart 1.45.0
* OPA 1.21.3, opa-kube-mgmt chart 11.0.14

## [1.0.1](https://github.com/OKDP/platform-packages/compare/trino/v1.0.0...trino/v1.0.1) (2026-09-25)


### Bug Fixes

* replace release please anotation with custom release increment ([99c6bdc](https://github.com/OKDP/platform-packages/commit/99c6bdc8b8158dea5fcb1a49107529d35808cdb9))
