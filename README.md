# Postgresql
Base de Datos Relacional Postgresql

* [Instalar PostgreSQL](guia/installpostgresql.rst)
* [PostgreSQL File Structure](guia/filestructure.rst)
* [Parametros de configuracion segun el system](guia/parametroconf.rst)
* [Cambiar la ubicación de la carpeta de datos de PostgreSQL](guia/cambiarubicacion.rst)
* [Backup and Restore](guia/backuprestore.rst)



Cambiar la ubicación de la carpeta de datos de PostgreSQL

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



https://chachocool.com/como-instalar-postgresql-en-debian-10-buster/

