FROM postgres:14.1

RUN buildDependencies="libsybdb5 \
	freetds-dev \
	freetds-common \
    wget \
    gcc \
    make \
    postgresql-server-dev-$PG_MAJOR" \
  && apt-get update \
  && apt-get install -y ${buildDependencies} \ 
  && wget https://github.com/tds-fdw/tds_fdw/archive/v2.0.2.tar.gz \
  && tar -xvzf v2.0.2.tar.gz \
  && cd tds_fdw-2.0.2/ \
  && make USE_PGXS=1 \
  && make USE_PGXS=1 install \
  && echo "\n[mssql]\n\thost = mssql\n\tport = 1433\n\ttds version = 7.4\n\tread-only intent = yes\n" >> /etc/freetds/freetds.conf \
  && echo "[default]\n\tdate format = %b %e %Y %I:%M:%S.%z%p\n" > /etc/freetds/locales.conf \
