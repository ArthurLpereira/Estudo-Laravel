A primeiro rota ::get é para retornar a view onde vai ter o formulário. A segunda ::post é para enviar os dados para o Banco de Dados 
```php
    Route::get('/create', [NomeController::class, 'create'])->name('NomeQuePreferir-create');
    // Não vai dar confilito só a / pq são metodos diferentes
    Route::post('/', [NomeController::class, 'store'])->name('NomeQuePreferir-store');
```