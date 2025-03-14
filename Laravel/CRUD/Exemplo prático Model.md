tag: #Laravel 

Nossa model chama Jogo, e vamos mostrar o nome, categoria, o ano que foi criado e o valor.

```php
<?php

namespace App\Models;

use Illuminate\Database\Eloquent\Model; 

class Jogo extends Model
{
    protected $fillable = [
        'nome',
        'categoria',
        'ano_criacao',
        'valor',
    ];
}
```