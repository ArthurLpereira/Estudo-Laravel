tag: #Laravel 

```php
<?php 

namespace App\Http\Controllers;

use App\Models\Jogo;

use Illuminate\Http\Request; 

class JogosController extends Controller
{
    public function mostrar_tela(){
        $jogos = Jogo::all();

        return view('jogos.index', ['jogos'=>$jogos]);
    }
}
```