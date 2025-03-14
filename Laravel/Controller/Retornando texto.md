tag: #Laravel 

Função básica para retornar um "Olá mundo!"

```php
<?php

namespace App\Http\Controllers;

use Illuminate\Http\Request;

// Controller basico para teste
class JogosController extends Controller
{
    public function mostrar_tela(){
        // Para chamar um texto
        echo 'Olá mundo!';
    }

}
```