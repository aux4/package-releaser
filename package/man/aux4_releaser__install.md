#### Description

The `install` command automates the process of building and installing a local version of an aux4 package. It reads the package definition from the specified directory, temporarily updates the package version with a `-local` suffix, and generates a zip artifact using the aux4 pkger tool. The command then uninstalls any existing version, installs the freshly built local package, restores the original version in the `.aux4` file, and optionally removes the local zip file based on the provided flag.

#### Usage

```bash
aux4 aux4 releaser install [--dir <path>] [--rm <true|false>]
```

--dir   The directory containing the `.aux4` package definition (default: `.`)
--rm    Remove the generated local zip file after installation (default: `false`)

#### Example

```bash
aux4 aux4 releaser install --dir ./my-package --rm true
```

This command will perform the following steps:
1. Read the `.aux4` file in `./my-package` and determine the current version.
2. Update the version to `<current>-local` and build the package into a zip file.
3. Uninstall any previously installed version of this package.
4. Install the newly built zip via aux4 pkger.
5. Restore the original version in the `.aux4` file.
6. Remove the local zip file (`--rm true`).

```text
The package aux4/package-releaser:0.0.18-local has been installed
```