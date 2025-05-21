#### Description

The `install` command in the `aux4:releaser` profile is used to install a local version of the package. It reads the `.aux4` file to retrieve package information, builds the package, installs it locally, and then sets the version of the installed package.

#### Usage

```bash
aux4 install --dir <directory> --rm <true/false>
```

- `--dir <directory>`: The directory of the package. Default is the current directory.
- `--rm <true/false>`: Optional parameter to remove the package file after installation. Default is `false`.

#### Example

```bash
aux4 install --dir /path/to/package --rm true
```

```
The package aux4/package-releaser:0.0.15-local has been installed
```