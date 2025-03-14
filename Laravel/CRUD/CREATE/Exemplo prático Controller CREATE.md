```php
<?php

namespace App\Http\Controllers;

use App\Models\Jogo;

use Illuminate\Http\Request;

  

// Controller basico para teste
class JogosController extends Controller
  
    public function create(){
        return view('jogos.create');
    }

    public function store(Request $request){
        // Fazer esse teste para saber se o request está funcionando (ainda n está mandando para o banco)
        // dd($request);
        
        // Vai salvar todo o request no banco
        Jogo::create($request->all());
        
        // Redireciona para o jogos-index depois de salvar
        return redirect()->route('jogos-index');
    }
}
```