# RAILS
- Ruby 2.7
- PostgreSQL

## Pre-build
```bash
$ docker-compose run web rails new . --force --no-deps --database=postgresql
```

<br>

List the files
```bash
$ ls -l
```

<br>

If new files are owned by root, change the ownership of the new files
```bash
$ sudo chown -R $USER:$USER .
```

## First build
```bash
$ docker-compose build
```

## Connect database
Replace the contents of `config/database.yml` with the following:
```
default: &default
  adapter: postgresql
  encoding: unicode
  host: db
  username: postgres
  password:
  pool: 5

development:
  <<: *default
  database: myapp_development


test:
  <<: *default
  database: myapp_test
```
## Time to boot
```bash
$ docker-compose up
```

## Post-installation
Finally, you need to create the database. In another terminal, run:
```
$ docker-compose run web rake db:create
```
