tag: #Laravel 

Função básica para retornar uma view

```php
<?php

namespace App\Http\Controllers;

use Illuminate\Http\Request;

// Controller basico para teste
class JogosController extends Controller
{
    public function mostrar_tela(){
        // Para chamar uma view
         return view('jogos');
    }

}
```