tag: #Laravel 

Para mudar de rota é necessário colocar o nome em que foi colocado na rota entre as {{}} no href
``` HTML
<!DOCTYPE html>

<html lang="pt-br">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Jogos</title>
</head>
<body>
    <header>
        <h1>Bem vindo a página de jogos</h1>
    </header>
    <main>
        <!-- Mudando de página com nomenclatura -->
         <a href="{{ route ('home-index') }}">Clique</a>
    </main>
</body>
</html>
```