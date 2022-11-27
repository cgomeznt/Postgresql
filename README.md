# Postgresql
Base de Datos Relacional Postgresql

* [Instalar PostgreSQL](guia/installpostgresql.rst)
* [PostgreSQL File Structure](guia/filestructure.rst)
* [Parametros de configuracion segun el system](guia/parametroconf.rst)

los siguientes fs

  /postgres/binarios

  /postgres/data

  /postgres/log

  /postgres/wal

  /postgres/backup

  Binarios donde estarán los binarios de postgres

  Data, los archivos físicos de la base de datos

  El log, el log de base de datos, y los de auditoria si lo activa

  Los wal de los log trasanccionales, tipo los archive de oracle

  backup para los respaldos

  Binarios 10gb

  Data depende de cuanto estiman crecer con 15 puede ir bien.

  Log con 10gb estaría bien (hasta menos)

  El wall de 40gb,depende de los tamaños que defina en el postgres.cnf

  Y los backup con 10gb estaría bien, si crece el data, este debe aumentar tambien



https://www.postgresql.org/docs/current/storage-file-layout.html

https://www.oreilly.com/library/view/the-database-hackers/9780764578014/ch024-sec005.html#:~:text=Configuration%20files%20and%20the%20databases,PGDATA%20directory%20contains%20three%20subdirectories.

https://pgtune.leopard.in.ua/

https://chachocool.com/como-instalar-postgresql-en-debian-10-buster/

https://openwebinars.net/blog/instalar-postgresql/
