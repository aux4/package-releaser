#### Description

The `dev-publish` command builds and publishes the package's **current** version to the hub without any Git operations (no pull, no version bump, no commit, no tag, no push) and without incrementing the version. It is intended for publishing to a development hub (or any hub) when a full Git release is not wanted — for example, seeding a dev hub while a working tree still has uncommitted changes.

Like `release`, it routes the package to the correct repository:

- If the package `.aux4` declares a `repository` field (for example `"repository": "system"`), it publishes there with `--repository <that>`.
- Otherwise, if the package is marked `"private": true`, it publishes to the `private` repository.
- Otherwise it publishes to the default `public` repository.

Point it at a specific hub with the `AUX4_REGISTRY_URL` environment variable.

#### Usage

```bash
aux4 aux4 releaser dev-publish [--dir <directory>] [--noBuild <true|false>]
```

--dir      The directory of the package (default: `.`)
--noBuild  Skip the build step (default: `false`)

#### Example

Publish the current version of a package to a development hub:

```bash
AUX4_REGISTRY_URL="https://dev.api.hub.aux4.io/v1/packages" \
  aux4 aux4 releaser dev-publish --dir packages/my-package/package
```

```text
building version 0.0.8
publishing version 0.0.8 --repository system
The package aux4/my-package:0.0.8 has been published (no git, no version bump)
```
