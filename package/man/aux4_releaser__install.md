#### Description

The `install` command in the `aux4:releaser` profile is used to install a local version of the package. It reads the `.aux4` file, retrieves the necessary information, builds the package, installs it locally, and updates the version accordingly. By executing this command, users can easily install a local version of the package for testing or development purposes.

#### Usage

```bash
aux4 install --dir <directory_path> --rm <true_or_false>
```

- `dir`: The directory of the package. (Default: current directory `.`)
- `rm`: Remove the package file after installation. (Default: false)

#### Example

Installing a local version of the package in the current directory without removing the package file:

```bash
aux4 install
```

This command will install the local version of the package in the current directory without deleting the package file.

```
The package aux4/package-releaser:version-local has been installed
```