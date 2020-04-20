# Request

El Request es el que contendrá la información que llega cuando alguien hace una petición al servidor. Se podrán traer parámetros get, datos de formulario en post o datos en la URL.

- Laravel utiliza inyección de dependencias y cuando detecta que se recibe una variable request, sabe que debe inyectar el request que está accediendo a la acción.

- Contamos con un helper muy útil de Laravel que reemplaza el var_dump y el die; este helper es dd.


### Ejemplo desde el controller
```php

    
    <?php

    namespace App\Http\Controllers;

    use Illuminate\Http\Request;

    class DashboardController extends Controller
    {
        // http://localhost:8000/Dashboard?title=test%20title
        public function index(Request $request)
        {
            $title = $request->query('title', null);

            return view('dashboard')->with('title',$title);
        }
    }
```