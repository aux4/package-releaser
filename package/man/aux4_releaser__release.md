#### Description

The `release` command automates the entire process of publishing a new version of your package. It starts by pulling the latest changes from the repository, then reads the current version from the package metadata and increments it according to the specified semver level. After updating the version, it builds and packages the project, publishes the artifact to the package registry, and finally creates a corresponding git tag and GitHub release. Upon completion, local build files are cleaned up and a confirmation message indicates that the release was successful.

#### Usage

```bash
aux4 aux4 releaser release --dir <path> --level <patch|minor|major>
```

--dir   Specifies the directory of the package (default: current directory).
--level Defines the semantic version increment level: patch, minor, or major.

#### Example

This example releases a new minor version of the package from the current directory:

```bash
aux4 aux4 releaser release --level minor
```

It will pull the latest commits, bump the version (for instance from `1.2.3` to `1.3.0`), rebuild and publish the package, tag and release on GitHub, then remove temporary artifacts.

```text
next
building version 1.3.0
publishing version 1.3.0
tagging version 1.3.0
The package aux4_package-releaser:1.3.0 has been released
```