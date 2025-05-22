#### Description

The `tag` command is a part of the `aux4:releaser` profile and is responsible for creating a Git tag and a corresponding GitHub release for the specified package. It retrieves the current version defined in the `.aux4` configuration file, commits any changes with a message that includes the version number, and generates an annotated Git tag. Following that, it pushes the tag to the remote repository and creates a GitHub release that packages the necessary files for distribution.

This command assists in versioning and releasing software packages by automating the processes of tagging in Git and publishing releases on GitHub, ensuring that the releases are properly documented and easy to access.

#### Usage

Describe the main parameters and options of the command.

```bash
aux4 tag --dir <directory> --package <package_name>
```

#### Example

In this example, we will call the `tag` command and specify a directory for the package as well as its name.

```bash
aux4 tag --dir . --package aux4_package
```

This execution will create a Git tag for the current version of the package located in the specified directory and name it `aux4_package`. It will log the creation of the Git tag and push it to the remote repository, while also creating a corresponding GitHub release.

```
create git tag
create git release
```