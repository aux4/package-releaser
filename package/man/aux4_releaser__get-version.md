#### Description

The `get-version` command is used to retrieve the current version of the application or package that is being managed. It interfaces with the release management system to fetch the version details, ensuring that users can confirm the version they are working with in their deployments or development.

This command is particularly useful for automated scripts and CI/CD pipelines, as it provides a straightforward way to programmatically access version information without needing to manually inspect files or configurations.

#### Usage

Describe the main parameters and options of the command.

```bash
aux4 get-version
```

#### Example

To fetch the current version of the application, you would run the following command:

```bash
aux4 get-version
```

This command will output the version string of the current application or package being handled.

```text
1.0.0
```