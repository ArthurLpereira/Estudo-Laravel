View (Página Filha):index.blade.php (Página de Listar)
```php
@extends ('layouts.app')

@section('title', 'Listagem')

@section('content')

<div class="container mt-5">
<div class="row">
  <div class="col-sm-10">
    <h1>  Listagem dos Jogos</h1>
  </div>

  <div class="col-sm-2">
    <a href="{{route ('jogos-create')}}" class="btn btn-success">Novo Jogo</a>
  </div>
</div>
<table class="table">
  <thead>
    <tr>
      <th scope="col">#</th>
      <th scope="col">Nome</th>
      <th scope="col">Categoria</th>
      <th scope="col">Criação</th>
      <th scope="col">Valor</th>
      <th scope="col">Ações</th>
    </tr>
  </thead>
  <tbody>
        @foreach($jogos as $jogo)
            <tr>
                <th scope="row">{{ $jogo->id}}</th>
                <th scope="row">{{ $jogo->nome}}</th>
                <th scope="row">{{ $jogo->categoria}}</th>
                <th scope="row">{{ $jogo->ano_criacao}}</th>
                <th scope="row">{{ $jogo->valor}}</th>
                <th scope="row" class="d-flex"><a href="{{ route('jogos-edit', ['id'=>$jogo->id])}}" class="btn btn-primary me-2">Editar</a>

				//Aqui o metodo de deletar aplicado
				<form action="{{route('jogos-destroy', ['id' =>$jogo->id])}}" method="POST">
                  @csrf
                  @method('DELETE')
                  <button type="submit" class="btn btn-danger">Deletar</button>
                </form>
              </th>
            </tr>
        @endforeach
  </tbody>
</table>
</div>
@endsection
```