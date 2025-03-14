tag: #Laravel 

Layout (Template Mestre): app.blade.php
```php
<!DOCTYPE html>
<html lang="pt-br">
<head>
    <meta charset="UTF-8">
    <meta name="vi ewport" content="width=device-width, initial-scale=1.0">
    //Bootstrap opcional
    <link href="https://cdn.jsdelivr.net/npm/bootstrap@5.3.3/dist/css/bootstrap.min.css" rel="stylesheet" integrity="sha384-QWTKZyjpPEjISv5WaRU9OFeRpok6YctnYmDr5pNlyT2bRjXh0JMhjY6hW+ALEwIH" crossorigin="anonymous">
    <title>@yield('TituloQueQuiser')</title>
</head>
<body>

    @yield('NomeQueQuiser')
    
    //Bootstrap opcional
    <script src="https://cdn.jsdelivr.net/npm/bootstrap@5.3.3/dist/js/bootstrap.bundle.min.js" integrity="sha384-YvpcrYf0tY3lHB60NNkmXc5s9fDVZLESaAA55NDzOxhy9GkcIdslK1eN7N6jIeHz" crossorigin="anonymous"></script>
</body>
</html>
```

View (Página Filha):create.blade.php
```php
@extends ('layouts.app')

@section('title', 'Crie um jogo')

@section('content')

<div class="container">
    <h1>Crie um novo jogo</h1>
    <hr>
    <form action="{{route ('RotaEnviarParaoBanco')}}" method="POST">
        @csrf
		//Form do jeito que preferir
		//Colocar no name e for o mesmo nome da tabela no Banco para evitar problemas
    </form>
</div>

@endsection
```