# docker-postgres-tds-fdw

* **Author:** Valery Kirychenka
* **Name:** docker-postgres-tds-fdw

## About
Official [PostreSQL docker image](https://hub.docker.com/_/postgres/) with [TDS foreign data wrapper](https://github.com/tds-fdw/tds_fdw)

## Build status
[![Docker Automated buil](https://img.shields.io/docker/automated/jrottenberg/ffmpeg.svg)](https://hub.docker.com/r/valeryk/docker-postgres-tds-fdw/builds/)

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

***NOTE:*** **by default is used TDS version 7.0**
