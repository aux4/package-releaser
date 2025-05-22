#### Description

The `increment-version` command streamlines the process of bumping the version number in your package's `.aux4` manifest. It reads the current version, asks for confirmation, applies a SemVer increment at the specified level (patch, minor, or major), logs the new version, and updates the manifest accordingly.

#### Usage

```bash
aux4 aux4 releaser increment-version --dir <directory> --level <level>
```

- `--dir`: The directory containing the `.aux4` manifest (defaults to current directory).
- `--level`: The SemVer release level: `patch`, `minor`, or `major`.

#### Example

Increment the patch version in the current directory:

```bash
aux4 aux4 releaser increment-version --level patch
```

When you run this command, you'll be prompted for confirmation:

```text
Are you sure you want to release a new version? (y/n)
```

Assuming your current version is `0.0.19` and you confirm, the output will be:

```text
releasing version 0.0.20
```

The `.aux4` file is then updated to reflect the new version.