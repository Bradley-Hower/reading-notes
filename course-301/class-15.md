# *Course 301, Entry 15: Authentication*

## OAuth

### What is OAuth?

OAuth is an open-standard authorization framework (protocol for version 1.0) which allows unrelated servers to autenticate a user and then share authorization between them without sharing the authentication credentials (password or other signon method). It is like a valet key for a car.

### Give an example of what using OAuth would look like

A user wants to access a website. The website wants to limit access to those that have signed up. The user can then select to log in from another service provider. The service provider provides limited access to the user's information. Thus, the user can sign in to two services, without exposing their login credentials.

### How does OAuth work? What are the steps that it takes to authenticate the user?

1. The target site of interest connects on the backend to the signon credentials site.

2. The signon site generates a one-time token and secret. Which is handed to the user via the target site.

3. The user's software then forwards this to the authorization provider (sometimes is the signon site).

4. The user then is asked to sign in if not already logged in, and then asked to authorize the limited shared access. The user is given an access token as a result.

5. The user then gives this token to the target site.

6. The target site returns this token to the signon site as proof of authorization.

7. The signon site shares the limited access.

### What is OpenID?

OpenID was an authentication-based single sign-in. Now, OpenID works together with OAuth.

## Things I want to know more about

Why TLS was not implemented by default. What other authentication standards are being worked on.
