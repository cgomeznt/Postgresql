# Postgresql
Base de Datos Relacional Postgresql

* [Instalar PostgreSQL](guia/installpostgresql.rst)
* [PostgreSQL File Structure](guia/filestructure.rst)
* [Parametros de configuracion segun el system](guia/parametroconf.rst)
* [Cambiar la ubicación de la carpeta de datos de PostgreSQL](guia/cambiarubicacion.rst)
* [Backup and Restore](guia/backuprestore.rst)



Cambiar la ubicación de la carpeta de datos de PostgreSQL

FileSystem su tamaño

  /postgres/binarios  - 10Gb  - donde estarán los binarios de postgres

  /postgres/data      - 15Gb  - los archivos físicos de la base de dato, depende de cuanto estiman crecer con 15 puede ir bien

  /postgres/log       - 10Gb  - log de base de datos, y los de auditoria si lo activa, Log con 10gb estaría bien (hasta menos)

  /postgres/wal       - 40Gb  - wal de los log trasanccionales, tipo los archive de oracle, depende de los tamaños que defina en el postgres.cnf

  /postgres/backup    - 15Gb  - backup para los respaldos, por lo general siempre sera igual el tamaño que de data




https://chachocool.com/como-instalar-postgresql-en-debian-10-buster/

