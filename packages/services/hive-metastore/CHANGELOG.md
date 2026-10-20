# Changelog

## 2.0.0 (2026-10-21)


### ⚠ BREAKING CHANGES

* the package version no longer embeds the upstream version: the tag is `2.0.0`, the upstream version is `appVersion` in the descriptor
* the parameters are a closed JSON Schema: an unknown parameter is refused
* the roles `metastore-catalog` and `data-catalog` are renamed `okdp.io/hive-metastore` and `okdp.io/data-catalog`; the dependencies on `database-server` and `storage` are dropped, the database and the object store are connections; the package depends on `okdp.io/secrets-backend` for the Secrets it names
* `db` and `storage` are plain strings naming the database-server and s3 Connections, read through `inputs` entries

### Features

* describe the package with contract 0.2

## [1.0.1](https://github.com/OKDP/platform-packages/compare/hive-metastore/v1.0.0...hive-metastore/v1.0.1) (2026-09-25)


### Bug Fixes

* replace release please anotation with custom release increment ([99c6bdc](https://github.com/OKDP/platform-packages/commit/99c6bdc8b8158dea5fcb1a49107529d35808cdb9))
