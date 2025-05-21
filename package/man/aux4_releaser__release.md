#### Description

The `release` command allows you to release a new version of the package. It automates the process of incrementing the package version, building the package, publishing it, tagging the release, and completing the release process. By specifying the level of the release as either `patch`, `minor`, or `major`, you can easily manage versioning.

#### Usage

```bash
aux4 release --dir <directory> --level <patch|minor|major>
```

#### Example

```bash
aux4 release --dir ~/my-package --level minor
```

```
Next
Building version X.Y.Z
Publishing version X.Y.Z
Tagging version X.Y.Z
The package {scope}/{name}:X.Y.Z has been released
```