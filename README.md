# DEV-POSTMAN

This repository contains Postman collections and template environments that demonstrate usage of the core Volustor APIs.

```
/auth       - Signin, Signout, Sessions
/manifest   - Leases, Objects
/portal     - Accounts, Assets, Projects, Stages, Users, Watchers
/queue      - Pipelines, Jobs
```

These collections are designed to demonstrate "machine-to-machine" communication secured via a JWT access_token in the header of every request.

To interact with these collections you'll first need an API "Client Id" and "Client Secret" issued by Volustor during account creation.  Please contect [support@volustor.xyz](email:support@volustor.xyz) for more details.

## Authentication


```bash
curl --request POST \
  --url "https://{{env}}-volustor.us.auth0.com/oauth/token" \
  --header "content-type: application/json" \
  --data "{
    'client_id':'{{client_id}}',
    'client_secret':'{{client_secret}}',
    'audience':'https://api.{{env}}.volustor.xyz',
    'grant_type':'client_credentials'
  }"
```

## Usage

```bash
curl --request GET \
    --url <Your API Endpoint> \
    --header 'authorization: Bearer <Your Access Token>'
```


