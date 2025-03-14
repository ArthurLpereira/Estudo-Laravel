```php
    public function destroy($id){
        Jogo::where('id',$id)->delete();
        return redirect()->route('jogos-index');
    }
```