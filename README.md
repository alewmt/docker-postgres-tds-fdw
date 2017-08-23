# docker-postgres-tds-fdw

* **Author:** Valery Kirychenka
* **Name:** docker-postgres-tds-fdw

## About
Official [PostreSQL docker image](https://hub.docker.com/_/postgres/) with [PostgreSQL foreign data wrapper](https://github.com/tds-fdw/tds_fdw)

## Environment Valiables
This images uses all variables from [PostreSQL image](https://hub.docker.com/_/postgres/)

In additianal to PostreSQL image variables, the image uses environment variables from [FreeTDS](http://www.freetds.org/userguide/envvar.htm):

 - FREETDS
 - TDSVER
 - TDSPORT
 - SYBASE
 - TDSQUERY, DSQUERY
 - TDSHOST

See [FreeTDS docs](http://www.freetds.org/index.html)
