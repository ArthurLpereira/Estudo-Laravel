tag: #Laravel 

Layout (Template Mestre): app.blade.php
```php
<!DOCTYPE html>
<html lang="pt-br">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
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

View (Página Filha):index.blade.php
```php
@extends ('Caminho/Arquivo')

@section('TituloQueQuiser', 'Teste') 

@section('NomeQueQuiser')

//Faça do jeito que quiser, só uma forma mais fácil. De preferencia faça algo bonito :)
<table class="table">
  <thead>
    <tr>
      <th scope="col">#</th>
      <th scope="col">Coluna01</th>
      <th scope="col">Coluna02</th>
      <th scope="col">Coluna03</th>
      <th scope="col">Coluna04</th>
    </tr>
  </thead>
  
  <tbody>
  
        @foreach($dados as $dado)
            <tr>
            //Dados01... Troque pelas colunas do banco (Com o nome identico)
                <th scope="row">{{ $dado->Dado01}}</th>
                <th scope="row">{{ $dado->Dado02}}</th>
                <th scope="row">{{ $dado->Dado03}}</th>
                <th scope="row">{{ $dado->Dado04}}</th>
                <th scope="row">{{ $dado->Dado05}}</th>
            </tr>
        @endforeach

  </tbody>
</table>
@endsection
```