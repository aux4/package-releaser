# package-releaser 0.1.5

## Repository-aware publishing

- The `release` command now routes the published package to the correct hub repository based on the package `.aux4`:
  - a `repository` field (for example `"repository": "system"`) publishes with `--repository <that>`;
  - otherwise a `"private": true` package publishes to the `private` repository;
  - otherwise it publishes to the default `public` repository.
  
  Previously `release` always published with the default `public` repository, which could publish a private package to the public repository.

## New `dev-publish` command

- Added `aux4 aux4 releaser dev-publish`, which builds and publishes the package's current version with **no** Git operations (no pull, version bump, commit, tag, or push). It honors the same `repository`/`private` routing as `release`. Point it at a specific hub with `AUX4_REGISTRY_URL`. Useful for seeding a development hub while a working tree still has uncommitted changes.
