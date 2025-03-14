```php
    Route::get('/create', [JogosController::class, 'create'])->name('jogos-create');
    // Não vai dar confilito só a / pq são metodos diferentes
    Route::post('/', [JogosController::class, 'store'])->name('jogos-store');
```