# DEV-POSTMAN

This repository contains Postman collections and template environments that demonstrate usage of Volustor's core APIs.

```
/auth       - Signin, Signout, Sessions
/manifest   - Leases, Objects
/portal     - Accounts, Assets, Projects, Stages, Users, Watchers
```

These collections are designed to demonstrate "machine-to-machine" communication, secured via JWT tokens.

To uses these collections you'll first need an API "Client Id" and "Client Secret" Issued by Volustor during your account creation process. Please contect [support@volustor.xyz](email:support@volustor.xyz) for more information.

## Usage

1. Import the collections and environments.

2. Update the required environment with your "Client ID" and "Client Secret".

3. Authenticate via the GetAccessToken method.

4. The generated access_token will then be automatically appended to the header of every future request.
