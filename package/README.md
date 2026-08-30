# aux4/package-releaser

Build, version, and publish aux4 packages to the hub.

## Installation

```bash
aux4 aux4 pkger install aux4/package-releaser
```

## Quick Start

Release a patch version of the current package:

```bash
aux4 aux4 releaser release --level patch
```

Install a local build for testing:

```bash
aux4 aux4 releaser install --dir ./my-package
```

## Commands

| Command | Description |
|---------|-------------|
| `aux4 aux4 releaser release` | Full release cycle: bump version, build, publish, tag |
| `aux4 aux4 releaser dev-publish` | Build and publish the current version with no Git operations or version bump |
| `aux4 aux4 releaser install` | Build and install a local version for testing |
| `aux4 aux4 releaser tag` | Create a Git tag and GitHub release |
| `aux4 aux4 releaser get-version` | Print the current package version |
| `aux4 aux4 releaser increment-version` | Bump the version in `.aux4` |
| `aux4 aux4 releaser aux4-login` | Authenticate to the aux4 hub via 1Password |

### release

Run a full release cycle: pull latest changes, increment the version, build and publish the package, and create a Git tag and GitHub release.

```bash
aux4 aux4 releaser release --level <patch|minor|major> [--dir <directory>]
```

The publish step routes the package to the correct repository: a `repository` field in the package `.aux4` (for example `"repository": "system"`) publishes there; otherwise a `"private": true` package publishes to the `private` repository; otherwise it publishes to the default `public` repository.

### dev-publish

Build and publish the package's current version to the hub with no Git operations (no pull, bump, commit, tag, or push). Honors the same `repository`/`private` routing as `release`. Point it at a specific hub with the `AUX4_REGISTRY_URL` environment variable. Useful for seeding a development hub while a working tree still has uncommitted changes.

```bash
aux4 aux4 releaser dev-publish [--dir <directory>] [--noBuild <true|false>]
```

### install

Build and install a local version of a package for testing. Appends `-local` to the version, builds a zip archive, and installs it.

```bash
aux4 aux4 releaser install [--dir <path>] [--rm <true|false>] [--force <true|false>]
```

| Flag | Description | Default |
|------|-------------|---------|
| `--dir` | Path to the package directory | `.` |
| `--rm` | Remove the zip file after installation | `false` |
| `--force` | Force the install via pkger `--force`, overriding the current version and ignoring dependents. Needed to reinstall a package other packages depend on | *(omitted)* |

**Note:** When other installed packages depend on the one you are reinstalling, pkger refuses the plain install. Use `--force true` to override the current version and ignore dependents so the local build takes effect.

### tag

Create a Git tag and GitHub release for the current package version.

```bash
aux4 aux4 releaser tag [--dir <directory>] --scope <scope> --name <name>
```

### get-version

Print the current version from the `.aux4` manifest.

```bash
aux4 aux4 releaser get-version [--dir <directory>]
```

### increment-version

Bump the version number in the `.aux4` manifest.

```bash
aux4 aux4 releaser increment-version --level <patch|minor|major> [--dir <directory>]
```

### aux4-login

Authenticate to the aux4 hub using credentials stored in 1Password.

```bash
aux4 aux4 releaser aux4-login --secret <1password-secret-path>
```

## License

Apache-2.0
