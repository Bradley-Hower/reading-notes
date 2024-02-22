# *Course 401 Python, Entry 33: Authentication & Production Server

**What is the primary purpose of JSON Web Tokens (JWTs) and how do they work in terms of encoding and decoding data?**

JWTs is primary used to authenticate a party member, whether it is a user or a service. If the party member is authenticated, certain authorizations can be granted. JWTS are great because they are so light-weight. In addition, information can be sent with JWTs due to the signature nature verifying it is from said entity.

JWTs work by using a public and private key. By itegrating these keys, a unique signature can be found which is would be immensly difficult to crack with today's technology. One can be sure the secret used to sign is safe, as it is a unique combination of the secret(private key) and a public key.

**How does JWT Authentication integrate with Django REST Framework to secure API endpoints, and what are the key components involved in this process?**

DRF uses djangorestframework_simplejwt to use JWTs. The key spots that need changed are settings and urls at the project level. Both of these implement the simplejwt library. For any information to served up from urls, authentication must be had. In addition to this, regular authentication must be implemented at the MTUV components.

Two tokens are required are the access and refresh token, both received from the api via HTTP POST request. These are stored locally.

The **access token** is important for any future requests. It will need to be included as the Bearer token following standard syntax within the body of any HTTP requests. The **refresh token** is used once the access token expires to obtain a new access token.

**Why is Django’s built-in runserver not suitable for production environments, and what are some alternative server options that should be considered for deploying a Django application?**

Reasons include:

- Like of security audits.
- `runserver` is slow.

In contrast, a productions setup is fast and reliable.

**web server** - used to quickly serve up static content. Ex: Nginx

**application server** - used to process. WSGI is an example specification. Ex: Gunicorn.

## Things I want to know more about

I want to learn more on how the sha256 algorithm works.
