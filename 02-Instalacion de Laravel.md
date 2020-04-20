# Instalación de Laravel

- Composer es un manejador de dependencias para PHP, así que todas las dependencias que necesitemos, incluído Laravel, serán instaladas por Composer.

- Para trabajar en Laravel necesitarás un servidor de PHP y una base de datos.

- Laravel nos ofrece un instalador que podemos traer a través de Composer y utilizaremos global en el comando para que la instalación se realice en toda la máquina virtual o computador.

-Podemos comprobar si Laravel quedó bien instalado usando el comando “laravel” el cual nos dará la versión del instalador y los comandos disponibles.

- El comando “new” nos ayuda a crear un nuevo proyecto de Laravel; al hacer esto se crearán las carpetas y estructura del proyecto y el archivo composer con las dependencias necesarias.

- Para trabajar con Laravel es necesario tener la versión de PHP 7.1 o superior.

- El comando “artisan” nos da una serie de comandos de Laravel, son muchos y no todos se utilizan pero es buena idea revisar la documentación y opciones disponibles.

- El comando “serve” levanta un servidor de PHP corriendo el proyecto actual, el cual nos arroja una dirección IP la cual abriéndola nos muestra nuestro proyecto.

## Instalar Laravel

1. Utilizando el comando de composer

        composer global require laravel/installer

2. Crear nuevo proyecto utilizando Laravel

        laravel new my-project

3. Ejecutar el proyecto

        php artisan serve