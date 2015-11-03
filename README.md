postgresql
=================

**Note:** There is now an [official Postgres image](https://registry.hub.docker.com/_/postgres/)

PostgreSQL 9.4

    $ docker run -d -p 5432:5432 -e POSTGRESQL_USER=bowwow -e POSTGRESQL_PASS=bowwow -e POSTGRESQL_DB=bowwow bowwow/postgresql9.4
    da809981545f
    $ psql -h localhost -U test test
    Password for user test:
    psql (9.4.2, server 9.4.4)
    SSL connection (cipher: DHE-RSA-AES256-SHA, bits: 256)
    Type "help" for help.

    ubuntu14.04=#

(Example assumes PostgreSQL client is installed on Docker host.)


## Environment variables

 - `POSTGRESQL_DB`: A database that is automatically created if it doesn't exist. Default: `docker`
 - `POSTGRESQL_USER`: A user to create that has access to the database specified by `POSTGRESQL_DB`. Default: `docker`
 - `POSTGRESQL_PASS`: The password for `POSTGRESQL_USER`. Default: `docker`
