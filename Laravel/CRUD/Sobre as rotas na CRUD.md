**TODAS** as rotas feitas precisam estar dentro de um grupo exemplo:

```php
// Todas as rotas que estiverem aqui dentro vão estar com o prefixo de jogos
Route::prefix('jogos')->group(function(){
	//Rota Listar

	//Rota Criar

	//Rota Deletar

	//Rota Alterar
});
```

Exemplo prático:
```php
// Todas as rotas que estiverem aqui dentro vão estar com o prefixo de jogos
Route::prefix('jogos')->group(function(){

    Route::get('/', [JogosController::class, 'index'])->name('jogos-index');
  
    Route::get('/create', [JogosController::class, 'create'])->name('jogos-create');

    // Não vai dar confilito só a / pq são metodos diferentes
    Route::post('/', [JogosController::class, 'store'])->name('jogos-store');
});
```