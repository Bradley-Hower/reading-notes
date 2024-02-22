# *Course 401 Python, Entry 34: API Deployment

**What are the key principles to follow when organizing and configuring Django settings for a project, according to the “Django Settings Best Practices” reading?**

Be aware of:

- Evironments. Django settings need to be maintained. Store configuration in the environment.
- Sensitive data. Database passwords and tokens are an issue.
- Settings need to be shared when developing as a team.
- Settings can have some non-obvious logic.

Django-environ is a great way to store sensitive information in a .env file.

Settings can be split up to other settings files.

**How does the White Noise library contribute to the efficient serving of static files in a Django application, and what are the steps to integrate it into a project?**

WhiteNoise allows content to served up with the best performance in comparison using services like Amazon S3. Why? Compression. Secondly, distributing data is much less complex using a CDN. Everything in WhiteNoise just moves via standard HTTP semantics.

## WhiteNoise Installation

1. `pip install whitenoise`
2. In settings:

```
MIDDLEWARE = [
    # ...
    "django.middleware.security.SecurityMiddleware",
    "whitenoise.middleware.WhiteNoiseMiddleware",
    # ...
]

STATICFILES_STORAGE = "whitenoise.storage.CompressedManifestStaticFilesStorage"
```

3. WSGI
```
from whitenoise import WhiteNoise

from my_project import MyWSGIApp

application = MyWSGIApp()
application = WhiteNoise(application, root="/path/to/static/files")
application.add_files("/path/to/more/static/files", prefix="more-files/")
```

**What is the purpose of Cross-Origin Resource Sharing (CORS) in web applications, and how can it be implemented and configured in a Django project to control access to resources?**

The purpose of CORS is to allow server-to-server requests on behalf of a user in the browser. CORS can be setup in Django via django-cors-headers. CORS preflight allows for even more refined validation prior to allowing any cross-origin request.

## Installing CORS Headers

1. `python -m pip install django-cors-headers`

2. In settings. For middleware, add the code as high as possible.

```
INSTALLED_APPS = [
    ...,
    "corsheaders",
    ...,
]

MIDDLEWARE = [
    ...,
    "corsheaders.middleware.CorsMiddleware",
    "django.middleware.common.CommonMiddleware",
    ...,
]
```

3. `CORS_ALLOWED_ORIGINS`

Set equal to a list of URLs that are allowed.

4. `CORS_ALLOWED_ORIGIN_REGEXES`

Similar to CORS_ALLOWED_ORIGINS, but variations thereof.

5. `CORS_ALLOW_ALL_ORIGINS`

A bool. Not recommended to allow.

More optional configurations at [https://pypi.org/project/django-cors-headers/](https://pypi.org/project/django-cors-headers/).

## Things I want to know more about

The different network inner-workings of WhiteNoise and technicals of why its better. A lot of jargon was dropped in that article.
