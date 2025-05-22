#### Description

The `tag` command automates marking a release in your git repository and creating a corresponding GitHub release. It reads the current version from the `.aux4` manifest, commits any outstanding changes with a standardized message, applies a semantic tag to the latest commit, pushes the tags upstream, and publishes a release on GitHub including the packaged zip file of the project.

#### Usage

```bash
aux4 aux4 releaser tag [--dir <path>] --package <scope_name>
```

--dir      Path to the package directory (default: `.`)
--package  Name of the package artifact, formatted as `<scope>_<name>`

#### Example

```bash
aux4 aux4 releaser tag --package aux4_package-releaser
```

This runs the tag command in the current directory (default), reads the version field from `.aux4` (e.g., `0.0.18`), commits with `release: 0.0.18`, creates and pushes the git tag `v0.0.18`, and then uses `gh` to publish a GitHub release `v0.0.18`, attaching the `aux4_package-releaser_0.0.18.zip` file.

```text
[master 1a2b3c4] release: 0.0.18
 1 file changed, 1 insertion(+)
create git tag
Tagged v0.0.18
Creating GitHub release v0.0.18...
```