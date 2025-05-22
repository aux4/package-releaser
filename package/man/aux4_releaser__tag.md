#### Description

The `tag` command streamlines the process of creating a versioned Git tag and corresponding GitHub release for a package managed by Aux4. It reads the current version from the package’s `.aux4` file, commits any staged changes with a standardized release message, then generates and pushes an annotated Git tag reflecting that version. Finally, it leverages the GitHub CLI to publish a release entry tied to the tag, packaging your built artifact for distribution.

By encapsulating these steps into a single command, `tag` ensures consistent release practices across projects. You can point it to any directory containing a `.aux4` manifest, and by supplying the package scope and name, it constructs the correct asset filename for the GitHub release.

#### Usage

The `tag` command uses the following options to locate your package and identify the release artifact:

  --dir <directory>     Path to the package directory (default: `.`)
  --scope <scope>       Package scope used to build the release asset name
  --name <package-name> Package name used to build the release asset name

```bash
aux4 releaser tag --dir <directory> --scope <scope> --name <package-name>
```

#### Example

The following example tags version `0.0.19` of a package located in the current directory, under the scope `aux4` and name `package-releaser`, then pushes the tag and creates a GitHub release with the ZIP asset.

```bash
aux4 releaser tag --scope aux4 --name package-releaser
```

This command reads the version from `./.aux4`, commits all staged changes as `release: 0.0.19`, creates and pushes the `v0.0.19` tag, and then uses `gh` to publish a release named `v0.0.19` with the corresponding ZIP archive.

```text
[main 1a2b3c4] release: 0.0.19
author: Your Name <you@example.com> 2024-06-01 12:34:56 +0000
 create git tag v0.0.19
 git push --follow-tags
 create git release v0.0.19
 ✓ Published release v0.0.19
```