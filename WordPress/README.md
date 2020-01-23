# WordPress ready with Apache PHP Server and MariaDB

## Source
[BeCode.org](https://github.com/becodeorg/LIE-Jepsen-2.14/tree/master/02-the-hill/03-wordpress/parcours/docker-compose)

<br>

### 1. Download and install WordPress
install it into the `DocumentRoot` directory

<br>

### 2. Fix WordPress > Permalink : 404 Page not found error
copy `localhost.conf` into the same directory as `docker-compose.yml`

<br>

### 3. Run server
``` bash
$ docker-compose up
```