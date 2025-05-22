#### Description

The `aux4-login` command automates authentication to the aux4 hub by retrieving stored credentials from a 1Password secret. It fetches the username and password fields, generates a one-time password (OTP), and then executes the aux4 login process in a single invocation. This eliminates manual entry of sensitive information and ensures secure, repeatable logins.

#### Usage

```bash
aux4 aux4 releaser aux4-login --secret <secret>
```

Where:

`--secret <secret>`  The 1Password secret path containing the `username`, `password`, and `otp` attributes required for login.

#### Example

```bash
aux4 aux4 releaser aux4-login --secret "op://MyVault/Aux4Hub"
```

This command reads the `username`, `password`, and `otp` values from the 1Password item at `op://MyVault/Aux4Hub` and logs in to the aux4 hub as the retrieved user:

```text
login to the aux4 hub alice@example.com
You are now logged in to aux4 hub.
```