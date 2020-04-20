# Controladores en Laravel

Basados en el modelo MVC, vimos que las vistas las tenemos en resources/views, igualmente en la carpeta app/Http/Controllers podremos definir nuestros controladores.
Aunque podemos utilizar closures directamente dentro de las rutas, Laravel viene preparado para que trabajemos con controladores.

- Cuando utilizamos el comando “artisan”, encontramos una sección llamada “make” que nos va a permitir crear diferentes cosas en el proyecto. make:controller nos crea un nuevo controlador.

- En nuestro archivo web.php, en la parte de los parámetros, en vez de poner un closure vamos a poner el nombre del controlador que creamos seguido de una @ y finalizando el método que llamaremos de ese controlador.


## Crear nuevo Controller

1. Crear controller

        php artisan make:controller HomeController


2. Crear una funcion dentro del controller

```php
<?php

namespace App\Http\Controllers;

use Illuminate\Http\Request;

class HomeController extends Controller
{
    public function index() {
        return view('welcome');
    }
}
```

3. Modificar la ruta 

```php
Route::get('/', 'HomeController@index');
```