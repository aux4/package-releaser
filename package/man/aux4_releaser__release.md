#### Description

The `release` command streamlines the full lifecycle of publishing a new version of your package in one seamless operation. It begins by synchronizing the local repository with its remote counterpart, reads and updates the version in your `.aux4` manifest according to the specified release level, and then triggers the build process. Once the build is complete it packages the project into a distributable archive, publishes it to the registry, and proceeds to tag the commit and create a corresponding GitHub release.

Throughout the execution it captures and logs each stage—pulling changes, version bump, build, publish, tagging, and cleanup—providing clear feedback on progress. By encapsulating all these steps, the `release` command ensures consistency and reduces manual effort when rolling out a new package version.

#### Usage

```bash
aux4 releaser release --level <patch|minor|major> [--dir <path>]
```

- `--level`: The semantic versioning level to bump (patch, minor, or major).
- `--dir`: (optional) Path to the package directory containing the `.aux4` file. Defaults to the current directory.

#### Example

The following example runs the release pipeline for the current directory, incrementing the minor version:

```bash
aux4 releaser release --level minor
```

This command will:
1. Pull the latest changes from the remote repository.
2. Bump the version in `.aux4` (e.g., from 1.2.3 to 1.3.0).
3. Build the project and package it as a zip file.
4. Publish the zip to the registry.
5. Tag the repository with `v1.3.0` and create a GitHub release.
6. Remove the local zip artifact.

```text
$ aux4 releaser release --level minor
> Pulling changes...
> Updating version to 1.3.0
> Building version 1.3.0
> Publishing version 1.3.0
> Tagging version 1.3.0 on GitHub
> Release complete: aux4/package-releaser:1.3.0
```