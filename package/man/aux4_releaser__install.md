#### Description

The `install` command is designed to facilitate the installation of auxiliary packages from the aux4 hub. It handles fetching the specified package based on the provided scope, name, and version, ensuring that the correct dependencies are met and set up appropriately for use in a project. The command takes user-defined parameters that allow for customization of the installation process and offers a streamlined experience for managing packages.

Using the `install` command enables users to leverage powerful tools and libraries seamlessly within their workflow. It integrates with the dynamic CLI developed by the aux4 package, allowing for efficient package management without the need for manual installation processes.

#### Usage

Describe the main parameters and options of the command.

```bash
aux4 install <scope>/<name>:<version>
```

#### Example

An example of how to use the `install` command is as follows:

```bash
aux4 install myscope/mypackage:1.0.0
```

This command will initiate the installation of the package `mypackage` version `1.0.0` under the scope `myscope`. The output will confirm the successful installation of the package and its dependencies.

```text
Installing myscope/mypackage:1.0.0...
Installation successful!
```