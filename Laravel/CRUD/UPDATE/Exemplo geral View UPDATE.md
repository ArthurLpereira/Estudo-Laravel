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

View (Página Filha):edit.blade.php
```php
@extends ('layouts.app')

@section('TituloQueQUiser', '...')

@section('NomeQueQuiser')

<div class="container">
    <h1>Edite seu jogo</h1>
    <hr>
    <form action="{{route ('NomeDaRota-update', ['id' => $variavel->id])}}" method="POST">
        @csrf
         //Precisa disso pois não tem metodo de PUT
        @method('PUT')
        <div class="form-group">
            <div class="form-group">
                <label for="nome">OqueVaiMudarnoInput1:</label>
                <input type="text" class="form-control" name="nome" placeholder="Digite um nome..." value="{{$variavel->OqueVaiMudarnoInput1}}">
            </div>
            <br>
            <div class="form-group">
                <label for="categoria">OqueVaiMudarnoInput2:</label>
                <input type="text" class="form-control" name="categoria" placeholder="Digite uma categoria para o jogo..." value="{{$variavel->OqueVaiMudarnoInput2}}">
            </div>
            <br>
            <div class="form-group">
                <label for="ano_criacao">OqueVaiMudarnoInput3:</label>
                <input type="number" class="form-control" name="ano_criacao" placeholder="Ano de criação..." value="{{$variavel->OqueVaiMudarnoInput3}}">
            </div>
            <br>
            <div class="form-group">
                <label for="valor">OqueVaiMudarnoInput4:</label>
                <input type="number" class="form-control" name="valor" placeholder="Digite um valor para o jogo..." value="{{$variavel->OqueVaiMudarnoInput4}}">
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