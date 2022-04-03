ARG MYSQL_VERSION
FROM mysql:${MYSQL_VERSION}

################################################
## database init
## 01-init.sql 不建議改檔名，這隻必須先執行才能 import db
################################################
ARG MYSQL_USER=${MYSQL_USER}
ARG INIT_SQL_FILE_NAME=01-init.sql
ARG INIT_DB_FLODER_NAME=docker-entrypoint-initdb.d

RUN echo "GRANT ALL PRIVILEGES ON *.* TO '${MYSQL_USER}'@'%';" >> /${INIT_DB_FLODER_NAME}/${INIT_SQL_FILE_NAME}

COPY ./config/my.cnf /etc/mysql/conf.d/my.cnf
RUN chmod 0444 /etc/mysql/conf.d/my.cnf

CMD ["mysqld"]

EXPOSE 3306
