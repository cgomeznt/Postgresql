Cambiar la ubicación de la carpeta de datos de PostgreSQL
==============================================================

Antes de cambiar la ubicación de los datos de PostgreSQL, primero verificaremos la configuración actual en el servidor PostgreSQL::

  sudo –u postgre psql

  postgres=# SHOW data_directory;
  Output:
     data_directory
  ------------------------------
  /var/lib/postgresql/15/main
  (1 row)
  postgres=#
  
Como podemos ver nuestro data_directory se encuentra configurado en /var/lib/postgresql/15/main. Antes de cambiar la ubicación paramos la base de datos::

  systemctl stop postgresql
  
Copiamos los datos::

  sync -av /var/lib/postgresql /psql
  
renombramos la carpeta::

   mv /var/lib/postgresql/15/main /var/lib/postgresql/15/main.bck
   
Ahora editamos la configuración de postgresq (/etc/postgresql/15/main/postgresql.conf) l y modificamos el atributo data_directory::

  vi data_directory = '/psql/postgresql/13/main' 
  
Iniciamos la base de datos::

  sudo systemctl start postgresql
  
Comprobamos nuevamente la configuaración::

  sudo –u postgre psql
  postgres=# SHOW data_directory;
        data_directory
  --------------------------
   /psql/postgresql/13/main
  (1 fila)

  postgres=#
