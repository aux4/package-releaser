#### Description

The `release` command in the aux4:releaser profile facilitates the process of preparing and deploying releases for a project or package. This command typically involves tasks such as version bumping, building artifacts, and possibly publishing them to a package registry. The command streamlines the release workflow, allowing developers to automate repetitive tasks involved in the release process.

When executed, the `release` command may accept various parameters that help customize the behavior of the release such as specifying the version number, the type of release (like patch, minor, or major), and additional flags that dictate the exact steps taken. By providing a clear structure and automated sequencing, this command enhances efficiency and minimizes errors associated with manual release processes.

#### Usage

Describe the main parameters and options of the command.

```bash
aux4 release --<variable> <value> --<variable> <value>
```

#### Example

To execute a release with a specific version and other options, you would run:

```bash
aux4 release --version 1.2.0 --release-type minor
```

In this example, the command initiates the release process for version 1.2.0 as a minor release. The expected output would confirm the details of the release and include any generated artifacts.

```text
Releasing version 1.2.0 as a minor update.
- Bumping version to 1.2.0
- Creating build artifacts...
- Publishing to the registry...
Release complete!
```