# Changelog

## 2.0.0 (2026-10-21)


### ⚠ BREAKING CHANGES

* the package version no longer embeds the upstream version: the tag is `2.0.0`, the upstream version is `appVersion` in the descriptor
* the parameters are a closed JSON Schema: an unknown parameter is refused
* the role `notebooks` is renamed `okdp.io/notebooks`; the dependencies are `okdp.io/ingress`, `okdp.io/certificate-manager`, `okdp.io/identity-provider` and `okdp.io/secrets-backend`, the object store is a connection
* `storage` is a plain string naming the s3 Connection, read through an `inputs` entry
* the kubauth client provisioning is removed, with the `oidc-client` module and the `oidc.kubauth` context key: `oidc.clientProvisioning` is `existing` (the OAuth client Secret `creds-<release>-oauth2` is provided) or `dcr`
* `oidc.clientProvisioning` defaults to `dcr`: the package registers its OAuth client unless the platform Context says `existing`
* `oidcRoleMapping` is replaced by `access`: `users` and `admins` list the groups allowed to sign in and made admins

### Features

* describe the package with contract 0.2
* register the OAuth client through dynamic client registration when the platform provisions clients that way
* JupyterHub 5.5.4, chart 4.4.4

### Bug Fixes

* stop reading `JUPYTERHUB_CRYPT_KEY` from the OAuth client Secret: the chart generates and keeps the auth state key, which overrode it

## [1.0.1](https://github.com/OKDP/platform-packages/compare/jupyterhub/v1.0.0...jupyterhub/v1.0.1) (2026-09-25)


### Bug Fixes

* replace release please anotation with custom release increment ([99c6bdc](https://github.com/OKDP/platform-packages/commit/99c6bdc8b8158dea5fcb1a49107529d35808cdb9))


### Refactoring

* remove disfunctioning minimal python image ([f37c1fd](https://github.com/OKDP/platform-packages/commit/f37c1fdfdde1939fe277fc3a22e440c0494acabf))
