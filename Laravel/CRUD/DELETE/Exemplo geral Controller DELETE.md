```php
    public function destroy($id){
        `NomeController`::where('id',$id)->delete();
        return redirect()->route('NomeQueQuiser-index');
    }
```