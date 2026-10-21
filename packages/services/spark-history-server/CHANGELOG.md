# Changelog

## 2.0.0 (2026-10-21)


### ⚠ BREAKING CHANGES

* the package version no longer embeds the upstream version: the tag is `2.0.0`, the upstream version is `appVersion` in the descriptor
* the parameters are a closed JSON Schema: an unknown parameter is refused
* the role `spark` is renamed `okdp.io/spark-history`; the dependencies are `okdp.io/ingress`, `okdp.io/certificate-manager`, `okdp.io/identity-provider`, `okdp.io/platform-tools` and `okdp.io/secrets-backend`, the object store is a connection
* `storage` is a plain string naming the s3 Connection, read through an `inputs` entry
* `roleMapping` accepts only `admin_groups`, `history_admin_groups`, `modify_groups` and `view_groups`

### Features

* describe the package with contract 0.2
* register the OAuth client through dynamic client registration when the platform provisions clients that way


### Bug Fixes

* generate the session cookie key per instance instead of shipping one fixed key

## [1.0.1](https://github.com/OKDP/platform-packages/compare/spark-history-server/v1.0.0...spark-history-server/v1.0.1) (2026-09-25)


### Bug Fixes

* replace release please anotation with custom release increment ([99c6bdc](https://github.com/OKDP/platform-packages/commit/99c6bdc8b8158dea5fcb1a49107529d35808cdb9))
