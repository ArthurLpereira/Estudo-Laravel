Layout (Template Mestre): app.blade.php
```php
<!DOCTYPE html>
<html lang="pt-br">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    //Bootstrap opcional
    <link href="https://cdn.jsdelivr.net/npm/bootstrap@5.3.3/dist/css/bootstrap.min.css" rel="stylesheet" integrity="sha384-QWTKZyjpPEjISv5WaRU9OFeRpok6YctnYmDr5pNlyT2bRjXh0JMhjY6hW+ALEwIH" crossorigin="anonymous">
    <title>@yield('title')</title>
</head>
<body>

    @yield('content')
    
    //Bootstrap opcional
    <script src="https://cdn.jsdelivr.net/npm/bootstrap@5.3.3/dist/js/bootstrap.bundle.min.js" integrity="sha384-YvpcrYf0tY3lHB60NNkmXc5s9fDVZLESaAA55NDzOxhy9GkcIdslK1eN7N6jIeHz" crossorigin="anonymous"></script>
</body>
</html>
```

View (Página Filha):edit.blade.php
```php
@extends ('layouts.app')

@section('title', 'Edite seu jogo')

@section('content')

<div class="container">
    <h1>Edite seu jogo</h1>
    <hr>
    <form action="{{route ('jogos-update', ['id' => $jogos->id])}}" method="POST">
        @csrf
        //Precisa disso pois não tem metodo de PUT
        @method('PUT')
        <div class="form-group">
            <div class="form-group">
                <label for="nome">Nome:</label>
                <input type="text" class="form-control" name="nome" placeholder="Digite um nome..." value="{{$jogos->nome}}">
            </div>
            <br>
            <div class="form-group">
                <label for="categoria">Categoria:</label>
                <input type="text" class="form-control" name="categoria" placeholder="Digite uma categoria para o jogo..." value="{{$jogos->categoria}}">
            </div>
            <br>
            <div class="form-group">
                <label for="ano_criacao">Ano de criação:</label>
                <input type="number" class="form-control" name="ano_criacao" placeholder="Ano de criação..." value="{{$jogos->ano_criacao}}">
            </div>
            <br>
            <div class="form-group">
                <label for="valor">Valor:</label>
                <input type="number" class="form-control" name="valor" placeholder="Digite um valor para o jogo..." value="{{$jogos->valor}}">
            </div>          
            <br>
            <div class="form-group">
                <input type="submit" class="btn btn-success" name="submit" value="Atualizar">
            </div>
        </div>
    </form>
</div>
  
@endsection
```