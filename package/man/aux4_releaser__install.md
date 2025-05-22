#### Description

The `install` command automates packaging and installing a local build of your aux4 package. It reads the project metadata from the `.aux4` file in the specified directory, temporarily appends a `-local` suffix to the version, and generates a zip archive via the aux4 pkger tool. After building, it uninstalls any existing version deployed from the hub, installs the freshly built local package, and then restores the original version in your project file. Optionally, you can remove the generated local artifact once the installation completes.

#### Usage

```bash
aux4 aux4 releaser install [--dir <path>] [--rm <true|false>]
```

--dir   The path to the directory containing your `.aux4` package definition (default: `.`)
--rm    Remove the generated local zip file after installation (`true` or `false`, default: `false`)

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