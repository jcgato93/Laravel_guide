# Cómo funcionan las Migraciones de DB

Laravel ofrece un sistema de migraciones de bases de datos las cuales pueden ser vistas como una especie de control de código pero para bases de datos. Esto es muy útil para equipos de trabajo al poder tener los cambios en el repositorio y de esta manera cada miembro del equipo podrá ejecutar las migraciones para tener los esquemas adecuados.

- Tenemos un comando llamado make:migration que nos permite generar archivos de migraciones.

- Contamos con una sección entera llamada migrate que nos servirá para realizar diferentes acciones relacionadas con las migraciones. Si ejecutamos migrate sin nada más, ejecutará todas las migraciones pendientes en el equipo.

- migrate:fresh va a borrar todas las tablas y las creará de nuevo utilizando todas las migraciones que tenemos.

- migrate:rollback nos permite regresar un paso.

Puedes encontrar las migraciones en la carpeta database/migrations. Laravel nos ofrece dos migraciones de inicio que son para crear tablas de usuarios y para crear una tabla de resets de passwords.
Las migraciones tienen dos partes:

- up, que nos dice qué va a crear la migración.

- down, que revierte lo que se hizo en la migración, activado al hacer rollback.

Al correr las migraciones se nos crearán 3 tablas, una de ella siendo migrations que nos llevará el control de cómo se va generando cada cambio.

Laravel nos ofrece Schema que nos trae diferentes cosas para trabajar sobre los sistemas de bases de datos.


### Ejecutar migraciones pendientes

        php artisan migrate