```php
    // Rota paara ir para a página de update
    Route::get('/{id}/edit', [JogosController::class, 'edit'])->where('id', '[0-9]+')->name('jogos-edit');
    //Rota para mandar a mudança para o banco
    Route::put('/{id}', [JogosController::class, 'update'])->name('jogos-update');
```