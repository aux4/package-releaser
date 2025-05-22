#### Description

The `release` command orchestrates a full release cycle for your package by pulling the latest changes, incrementing the version, building and publishing the artifact, and creating a Git tag and GitHub release. It encapsulates the entire workflow into a single command to ensure consistent and repeatable releases without manual intervention.

#### Usage

```bash
aux4 aux4 releaser release --level <patch|minor|major> [--dir <directory>]
```

#### Example

Release a minor update in the current directory:

```bash
aux4 aux4 releaser release --level minor
```

This will prompt you to confirm the release, bump the version in `.aux4`, build and publish the package archive to the registry, tag the release in Git and on GitHub, and finally clean up the artifact.

```text
? Are you sure you want to release a new version? (y/N) y
releasing version 0.0.20
next
building version 0.0.20
publishing version 0.0.20
log:tagging version 0.0.20
The package aux4/package-releaser:0.0.20 has been released
```