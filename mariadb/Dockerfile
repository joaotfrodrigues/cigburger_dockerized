FROM mariadb:10.4.32

COPY my.cnf /etc/mysql/conf.d/my.cnf

COPY mysql_data /var/lib/mysql

RUN chmod 644 /etc/mysql/conf.d/my.cnf
