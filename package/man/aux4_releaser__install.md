#### Description

The `install` command automates packaging and installing a local build of your aux4 package. It reads the project metadata from the `.aux4` file in the specified directory, temporarily appends a `-local` suffix to the version, and generates a zip archive via the aux4 pkger tool. After building, it uninstalls any existing version deployed from the hub, installs the freshly built local package, and then restores the original version in your project file. Optionally, you can remove the generated local artifact once the installation completes.

When other installed packages depend on the one you are reinstalling, pkger refuses the plain install (the package is in use, or the local version is considered older than the current one). Pass `--force true` to run the underlying `pkger install` with `--force`, which overrides the current version and ignores dependents so the local build takes effect. When `--force` is omitted (the default), the `--force` flag is not passed to pkger at all, preserving the original behavior.

#### Usage

```bash
aux4 aux4 releaser install [--dir <path>] [--rm <true|false>] [--force <true|false>]
```

--dir     The path to the directory containing your `.aux4` package definition (default: `.`)
--rm      Remove the generated local zip file after installation (`true` or `false`, default: `false`)
--force   Force the install via pkger `--force`, overriding the current version and ignoring dependents. Needed to reinstall a package other packages depend on (`true` or `false`; omitted by default, so pkger runs without `--force`)

#### Example

```bash
aux4 aux4 releaser install --dir ./my-package --rm true
```

This command will:
1. Load the version from `./my-package/.aux4`.
2. Update the version to `<current>-local` and build a zip artifact.
3. Uninstall any existing published version of this package.
4. Install the newly built local package using aux4 pkger.
5. Restore the original version string in `.aux4`.
6. Remove the local zip file, since `--rm true` was specified.

```text
The package aux4/package-releaser:0.0.19-local has been installed
```

To reinstall a package that other packages depend on, force the install:

```bash
aux4 aux4 releaser install --dir ./repository --force true
```