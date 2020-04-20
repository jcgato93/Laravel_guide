# Cómo funciona Blade

Internamente Laravel utiliza un motor de render llamado Blade y utilizamos este tipo motores porque PHP ha ido evolucionando más su parte de programación pero no tanto su parte de motores de templates. Algunas librerías han sido creadas para solventar esa falencia.

- En nuestras vistas podremos encontrar estructuras de control como @if o @auth que son helpers de Blade.

- Cuando queremos enviar información desde nuestras rutas a nuestras vistas podemos hacerlo mediante arreglos asociativos en el archivo web.php, los cuales pueden ser mostrados como variables en las vistas.

- No es recomendado usar PHP dentro de Blade ya que para esto contamos con los helpers.


## Cómo enviar data desde hacia las views

```php
Route::get('/test', function () {
    $name = 'Juan';
    
    return view('test')->with('name',$name);
});
```

```php
<div class="container">
    <h1>{{ $name ?? '' }}</h1>
</div>
```