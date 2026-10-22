# Changelog

## 2.0.0 (2026-10-21)


### ⚠ BREAKING CHANGES

* the package version no longer embeds the upstream version: the tag is `2.0.0`, the upstream version is `appVersion` in the descriptor
* the parameters are a closed JSON Schema: an unknown parameter is refused
* the role `spark` is renamed `okdp.io/spark-history`; the dependencies are `okdp.io/ingress`, `okdp.io/certificate-manager`, `okdp.io/identity-provider`, `okdp.io/platform-tools` and `okdp.io/secrets-backend`, the object store is a connection
* `storage` is a plain string naming the s3 Connection, read through an `inputs` entry
* `roleMapping` is replaced by `access`: `admin`, `historyAdmin`, `modify` and `view` list the groups granted each Spark ACL
* `oidc.clientProvisioning` defaults to `dcr`: the package registers its OAuth client unless the platform Context says `existing`
* the OIDC client is an `OIDCClient` object: in mode `dcr` its Secret is `<release>-oidc`, and the Context keys `oidc.dcr.registrationUrl` and `oidc.dcr.authMethod` give way to `oidc.dcr.provider` and `oidc.dcr.grantee`

### Features

* describe the package with contract 0.2
* register the OAuth client through dynamic client registration when the platform provisions clients that way
* register the OIDC client with the platform client registration (`okdp.io/identity-client-registration`), which removes it with the instance; the service starts once its client is ready; a client registered again is used after a restart of the instance

### Bug Fixes

* generate the session cookie key per instance instead of shipping one fixed key

## [1.0.1](https://github.com/OKDP/platform-packages/compare/spark-history-server/v1.0.0...spark-history-server/v1.0.1) (2026-09-25)


### Bug Fixes

* replace release please anotation with custom release increment ([99c6bdc](https://github.com/OKDP/platform-packages/commit/99c6bdc8b8158dea5fcb1a49107529d35808cdb9))
