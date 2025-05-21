#### Description

The `aux4-login` command allows users to log in to the aux4 hub using a 1Password secret. It retrieves the username and password from the specified 1Password secret, along with the OTP (One-Time Password) if available, and logs in to the aux4 hub with the provided credentials.

#### Usage

```bash
aux4 aux4-login --secret <secret>
```

#### Example

```bash
aux4 aux4-login --secret my_1password_secret
```
