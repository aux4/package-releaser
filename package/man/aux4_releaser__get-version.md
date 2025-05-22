#### Description

The `get-version` command retrieves the version field from the `.aux4` manifest in the specified directory. It uses `jq` to parse the `.aux4` JSON and outputs the version string, making it easy to integrate version checks into your scripts and workflows.

#### Usage

```bash
aux4 aux4 releaser get-version --dir <directory>
```

#### Example

Retrieve the version of the package in the current directory:

```bash
aux4 aux4 releaser get-version
```

This will output the current version, for example:

```text
0.0.19
```