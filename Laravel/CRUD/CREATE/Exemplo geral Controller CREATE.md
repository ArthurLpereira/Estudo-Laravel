```php
<?php

namespace App\Http\Controllers;

use App\Models\Jogo;

use Illuminate\Http\Request;

  

// Controller basico para teste
class NomeController extends Controller
  
    public function create(){
        return view('jogos.create');
    }

    public function store(Request $request){
        // Fazer esse teste para saber se o request está funcionando (ainda n está mandando para o banco)
        // dd($request);
        
        // Vai salvar todo o request no banco
        NomeModel::create($request->all());
        
        // Redireciona para alguma view depois de salvar
        return redirect()->route('CaminhoDaView');
    }
}
```