# Django + PostgreSQL

## Source
Official Docker Sample on [docker docs](https://docs.docker.com/compose/django/)

### 1. Clone the repo and open a new terminal

### 2. Create the Django project by running the docker-compose run command
``` bash
$ docker-compose run web django-admin startproject composeexample .
```
### 3. Change the ownership of the new files
``` bash
$ sudo chown -R $USER:$USER .
```
### 4. List the files just to verify
``` bash
$ ls -l
```
>> -rw-r--r--  1 user  staff  145 Feb 13 23:00 Dockerfile
>> drwxr-xr-x  6 user  staff  204 Feb 13 23:07 composeexample
>> -rw-r--r--  1 user  staff  159 Feb 13 23:02 docker-compose.yml
>> -rwxr-xr-x  1 user  staff  257 Feb 13 23:07 manage.py
>> -rw-r--r--  1 user  staff   16 Feb 13 23:01 requirements.txt

### 5. In your project directory, edit the `composeexample/settings.py` file.

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
```