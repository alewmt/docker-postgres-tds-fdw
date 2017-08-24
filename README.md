# docker-postgres-tds-fdw

* **Author:** Valery Kirychenka
* **Name:** docker-postgres-tds-fdw

## About
Official [PostreSQL docker image](https://hub.docker.com/_/postgres/) with [TDS foreign data wrapper](https://github.com/tds-fdw/tds_fdw)

## Build status
[![Docker Automated buil](https://img.shields.io/docker/automated/jrottenberg/ffmpeg.svg)](https://hub.docker.com/r/valeryk/docker-postgres-tds-fdw/builds/)

## Supported tags
- 9.6-1.0.8 (PostgreSQL 9.6 with TDF foreign data wrapper ver. 1.0.8)
- 9.5-1.0.8 (PostgreSQL 9.5 with TDF foreign data wrapper ver. 1.0.8)
- 9.4-1.0.8 (PostgreSQL 9.4 with TDF foreign data wrapper ver. 1.0.8)

## Instructions

### Run container
```bash
$ docker run --name some-postgres -e POSTGRES_PASSWORD=mysecretpassword -d postgres
```

### Install extension

#### via bash
```bash
psql -U postgres
postgres=# CREATE EXTENSION tds_fdw;
```

#### via any PostgreSQL client
```bash
CREATE EXTENSION tds_fdw;
```

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


