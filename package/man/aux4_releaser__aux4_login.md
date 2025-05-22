#### Description

The `aux4-login` command is designed to authenticate users within the aux4 framework. It streamlines the login process, allowing users to securely access their accounts and utilize the various functionalities offered by the platform. Upon execution, this command prompts for user credentials and verifies them against the stored records, ensuring a safe and efficient login experience.

This command not only manages user authentication but also integrates seamlessly with other commands in the `aux4:releaser` profile, enabling users to perform subsequent actions once logged in. The overall flow maintains a focus on user security and operational ease, making it essential for any interactions requiring user credentials.

#### Usage

The command can be executed with the following syntax:

```bash
aux4 aux4-login --<variable> <value> --<variable> <value>
```

#### Example

To log into your account, you can use the following command:

```bash
aux4 aux4-login --username your_username --password your_secure_password
```

This command prompts you to authenticate using the provided username and password. If successful, you will be granted access to your account, enabling you to utilize the further capabilities offered by the aux4 ecosystem.

```
Login successful!
Welcome, your_username!
```