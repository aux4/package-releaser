### `tag`

Create a git tag and a GitHub release.

#### Usage

```plaintext
aux4 aux4 releaser tag [options]
```

#### Description

The `tag` command creates a git tag and a GitHub release for the package. It performs the following actions:

1. Retrieves the version of the package from the `.aux4` file.
2. Commits the changes with a release message including the version.
3. Creates a git tag with the version number.
4. Pushes the changes with tags to the remote repository.
5. Creates a GitHub release with the tag and a zipped package.

#### Options

- `dir`: The directory of the package. Default is the current directory.
- `package`: The name of the package in the format `<scope>_<name>`.

#### Examples

- Create a git tag and GitHub release:
  ```plaintext
  aux4 aux4 releaser tag --package my_package
  ```
