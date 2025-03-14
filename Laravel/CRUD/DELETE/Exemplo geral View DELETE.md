Como o botão vai tomar uma ação é necessário fazer um formulário. 
```php
<form action="{{route('NomeQueQuiser-destroy', ['id' =>$variavel->id])}}" method="POST">
                  @csrf
     //Necessario pois não tem metodo de deletar
                  @method('DELETE')
                  <button type="submit" class="btn btn-danger">Deletar</button>
</form>
```