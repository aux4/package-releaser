#### Description

The `aux4-login` command allows users to authenticate and gain access to the aux4 system. It facilitates the login process by validating user credentials and establishing a session. Once invoked, it prompts the necessary user input and verifies that the credentials align with the system's records to ensure secure access.

This command is essential for enabling users to interact with the features provided by the aux4 framework, maintaining security while providing a smooth user experience during the login process.

#### Usage

Describe the main parameters and options of the command.

```bash
aux4 aux4-login --<variable> <value> --<variable> <value>
```

#### Example

Using the `aux4-login` command, a user can log into the system as follows:

```bash
aux4 aux4-login --username user123 --password pass123
```

In this example, the command attempts to log in the user with the username "user123" and the password "pass123". If the credentials are correct, the output would confirm successful authentication.

```text
Login successful! Welcome, user123.
```