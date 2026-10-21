# Changelog

## 2.0.0 (2026-10-21)


### ⚠ BREAKING CHANGES

* the package version no longer embeds the upstream version: the tag is `2.0.0`, the upstream version is `appVersion` in the descriptor
* the parameters are a closed JSON Schema: an unknown parameter is refused
* the role `okdp-server` is renamed `okdp.io/control-plane`
* the dependency on `ingress` is replaced by `okdp.io/identity-provider`: the server creates no ingress, it verifies the tokens of the platform identity provider

### Features

* describe the package with contract 0.2
* OKDP Control Plane Server 0.10.0

## [1.1.0](https://github.com/OKDP/platform-packages/compare/okdp-control-plane-server/v1.0.1...okdp-control-plane-server/v1.1.0) (2026-10-05)


### Features

* **control-plane-server:** consume the 0.9.0 release ([#100](https://github.com/OKDP/platform-packages/issues/100)) ([88b7193](https://github.com/OKDP/platform-packages/commit/88b71932bc703f179b991257588ecd49043a7c3b))

## [1.0.1](https://github.com/OKDP/platform-packages/compare/okdp-control-plane-server/v1.0.0...okdp-control-plane-server/v1.0.1) (2026-09-25)


### Bug Fixes

* replace release please anotation with custom release increment ([99c6bdc](https://github.com/OKDP/platform-packages/commit/99c6bdc8b8158dea5fcb1a49107529d35808cdb9))
