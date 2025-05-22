#### Description

The `tag` command is designed to facilitate the process of tagging releases within a project. It automates the workflow associated with versioning and helps ensure that releases are properly indexed and easy to manage. When executed, this command integrates seamlessly with your version control system and scripts the necessary steps to apply a tag to the latest commit, providing consistency across your release process.

By invoking this command, users can streamline their release management tasks, allowing them to quickly and effectively apply tags according to specified parameters. This is particularly useful in collaborative environments where multiple team members may be involved in the release process, ensuring that everyone stays aligned with proper versioning practices.

#### Usage

Describe the main parameters and options of the command.

```bash
aux4 tag --<variable> <value> --<variable> <value>
```

#### Example

```bash
aux4 tag --version v1.0 --message "Initial release"
```

This command applies a tag `v1.0` to the latest commit with the message "Initial release". It organizes the project's history by marking the release point in time, making it easy to reference and roll back if necessary.

```text
Tag 'v1.0' applied with message: Initial release
```