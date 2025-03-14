```php
    // Rota paara ir para a página de update
    Route::get('/{id}/edit', [NomeController::class, 'edit'])->where('id', '[0-9]+')->name('NomeQueQuiser-edit');
    Route::put('/{id}', [NomeController::class, 'update'])->name('NomeQueQuiser-update');
```