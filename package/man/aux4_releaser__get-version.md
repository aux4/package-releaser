#### Description

The `get-version` command retrieves the current version number defined in a package’s `.aux4` configuration file. By default, it reads the `.aux4` file in the specified directory and uses `jq` to extract the `version` field, then prints that version string to the console. This provides a simple, programmatic way to confirm the active version of your package, which is especially helpful in scripting and automation workflows.

#### Usage

```bash
aux4 aux4 releaser get-version [--dir <directory>]
```

--dir  The path to the directory containing the `.aux4` file. Defaults to the current directory (`.`).

#### Example

The following example fetches the version from the `.aux4` file in the current directory:

```bash
aux4 aux4 releaser get-version --dir .
```

This will output the version string defined in `.aux4`. For instance:

```text
0.0.18
```