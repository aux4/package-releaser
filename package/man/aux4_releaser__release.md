#### Description

The `release` command is a vital part of the package management and deployment process within the aux4 framework. It orchestrates a series of tasks to prepare a new version of the package by incrementing the version number, building the package, and publishing it to the package registry. After ensuring that the latest code is pulled from the repository, it intelligently detects the desired level of version increment, which can be a patch, minor, or major update.

This command not only manages versioning but also facilitates the entire release workflow by automating the build process and ensuring that the newly built version is properly published. It culminates in tagging the release in the version control system and cleaning up any temporary files, allowing for a seamless and efficient release cycle.

#### Usage

The command accepts several parameters to customize its behavior, particularly focusing on the directory of the package and the release level.

```bash
aux4 release --dir <directory> --level <patch|minor|major>
```

#### Example

To release a new minor version of your package located in the current directory, you would execute:

```bash
aux4 release --dir . --level minor
```

This command will increment the package version to the next minor version, build the package, publish it to the specified package registry, and tag the new version in your version control system. The expected output might indicate the version being published and the confirmation that the package has been released successfully.

```
The package <scope>_<name>:<version> has been released
```