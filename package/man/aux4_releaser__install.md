### Command: install

Install a local version of the package.

#### Usage:
```
aux4 aux4 releaser install --dir <directory> [--rm <true/false>]
```

- `--dir <directory>`: The directory of the package. Defaults to the current directory.
- `--rm <true/false>`: Optional. Remove the package file after installation. Defaults to `false`.

#### Example:
```bash
aux4 aux4 releaser install --dir /path/to/package --rm true
```

#### Description:
This command installs a local version of the package in the specified directory. By default, it installs the package in the current directory. Optionally, you can choose to remove the package file after installation by setting the `--rm` flag to `true`.