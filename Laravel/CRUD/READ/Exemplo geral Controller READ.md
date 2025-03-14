tag: #Laravel 

```php
<?php

namespace App\Http\Controllers;

use App\Models\NomeDoModel;

use Illuminate\Http\Request;

class NomeDoController extends Controller
{
    public function NomeFuncao(){
        $variavel =  Nome_do_seu_Model::all() //Mostrar tudo;
        // dd ($jogos);
        return view('nome_view', ['OqueÉ'=>$variavel]);
    }
}
```