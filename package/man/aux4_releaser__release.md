### Release Command

The `release` command in the `aux4:releaser` profile is used to release a new version of the package. This command performs the following steps:

1. Pull latest changes from the repository.
2. Increment the version of the package based on the specified release level (patch, minor, or major).
3. Get the updated version of the package.
4. Build the package.
5. Publish the built package to the aux4 hub.
6. Create a git tag and a github release for the new version.
7. Clean up by removing the intermediate package file.

#### Usage

```sh
aux4 aux4 releaser release --dir <directory> --level <release level>
```

- `--dir <directory>`: Path to the directory of the package. Default is the current directory.
- `--level <release level>`: Specifies the level of the release (patch, minor, or major).

#### Example

To release a new patch version of the package in the current directory:

```sh
aux4 aux4 releaser release --level patch
```
