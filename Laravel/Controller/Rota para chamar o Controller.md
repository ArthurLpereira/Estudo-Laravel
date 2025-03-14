tag: #Laravel 

Usar (importar) o arquivo do Controller no web.php
```php
use App\Http\Controllers\Nome_Arquivo;
```

Exemplo:
```php
use App\Http\Controllers\JogosController;
```

Exemplo geral:
```php
Route::get('/jogos',[Nome_Controller::class, 'função_criada_por_você']);
```

Exemplo prático:
```php
Route::get('/jogos',[JogosController::class, 'mostrar_tela']);
```

	- JogosController -> Nome do Controller
	- 'mostrar_tela' -> função que foi criada

