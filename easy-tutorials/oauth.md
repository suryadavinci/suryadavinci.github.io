# Oauth

## Parties involved
1. `Data Host` (ex: Facebook)
2. `Consumer` (ex: Farmville)
3. User

## Steps

1. `Consumer` registers their app with `Data Host`.
2. `Consumer` gets a `consumer_key` which is considered **public** and `consumer_token` which is **private**.
3. User wants to allow the `Consumer` to access their data.
4. `Consumer` redirects the user to a permissions page and the user is prompted to approve the request.
5. Upon approval, the `Data Host` redirects the user back to the `Consumer` with a `confirmation code`.
6. The `Data Consumer` makes an API call to the `Data Host` to exchange the `confirmation code` for an `access token`(In oauth 1.0 it is called an `access token secret`).

```
The resulting access token is the user-specific credential that can be used to make API calls.
```
