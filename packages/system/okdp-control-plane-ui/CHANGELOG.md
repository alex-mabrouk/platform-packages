# Changelog

## 2.0.0 (2026-10-21)


### ⚠ BREAKING CHANGES

* the package version no longer embeds the upstream version: the tag is `2.0.0`, the upstream version is `appVersion` in the descriptor
* the parameters are a closed JSON Schema: an unknown parameter is refused
* the role `okdp-ui` is renamed `okdp.io/ui`; the dependencies `okdp-server` and `ingress` become `okdp.io/control-plane` and `okdp.io/ingress`, plus `okdp.io/certificate-manager` and `okdp.io/identity-provider`
* `rolesClaim` is removed, the console reads the `groups` claim; `adminRole` is renamed `adminGroup`

### Features

* describe the package with contract 0.2

## [1.1.0](https://github.com/OKDP/platform-packages/compare/okdp-control-plane-ui/v1.0.1...okdp-control-plane-ui/v1.1.0) (2026-10-05)


### Features

* **control-plane-ui:** bump to release  0.9.1 ([#99](https://github.com/OKDP/platform-packages/issues/99)) ([451d09b](https://github.com/OKDP/platform-packages/commit/451d09b0b0b65502699ee18a831428a0ef1a664c))

## [1.0.1](https://github.com/OKDP/platform-packages/compare/okdp-control-plane-ui/v1.0.0...okdp-control-plane-ui/v1.0.1) (2026-09-25)


### Bug Fixes

* replace release please anotation with custom release increment ([99c6bdc](https://github.com/OKDP/platform-packages/commit/99c6bdc8b8158dea5fcb1a49107529d35808cdb9))
