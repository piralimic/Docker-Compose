# Django + PostgreSQL
<br>
<br>
## Source
Official Docker Sample on [docker docs](https://docs.docker.com/compose/django/)

<br>
<br>
### 1. Clone the repo and open a new terminal
> docker-compose.yml<br>
> Dockerfile<br>
> requirements.txt

<br>
<br>
### 2. Create the Django project by running the docker-compose run command
``` bash
$ docker-compose run web django-admin startproject composeexample .
```

<br>
<br>
### 3. Change the ownership of the new files
``` bash
$ sudo chown -R $USER:$USER .
```

<br>
<br>
### 4. List the files just to verify
``` bash
$ ls -l
```
> -rw-r--r--  1 user  staff  145 Feb 13 23:00 Dockerfile<br>
> drwxr-xr-x  6 user  staff  204 Feb 13 23:07 composeexample<br>
> -rw-r--r--  1 user  staff  159 Feb 13 23:02 docker-compose.yml<br>
> -rwxr-xr-x  1 user  staff  257 Feb 13 23:07 manage.py<br>
> -rw-r--r--  1 user  staff   16 Feb 13 23:01 requirements.txt

<br>
<br>
### 5. In your project directory
Edit the *`composeexample/settings.py`* file:

``` python
DATABASES = {
    'default': {
        'ENGINE': 'django.db.backends.postgresql',
        'NAME': 'postgres',
        'USER': 'postgres',
        'HOST': 'db',
        'PORT': 5432,
    }
}

# Internationalization
# https://docs.djangoproject.com/en/3.0/topics/i18n/

LANGUAGE_CODE = 'fr'

TIME_ZONE = 'Europe/Brussels'
```

<br>
<br>
### 5. Run server
``` bash
$ docker-compose up
```
