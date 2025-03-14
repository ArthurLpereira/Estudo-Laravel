tag: #Laravel 

Colocando parâmetros na view

```php
<?php

namespace App\Http\Controllers;

use Illuminate\Http\Request;

// Controller basico para teste
class JogosController extends Controller
{
    public function mostrar_tela(){
        // Retornar um view com parametros;
        $nome = 'Arthur';
        $id = '1';
        return view('jogos', ['nome'=>$nome, 'id'=>$id]);
    }

}
```