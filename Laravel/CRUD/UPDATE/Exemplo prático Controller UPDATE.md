```php
    public function edit($id){
        $jogos = Jogo::where('id', $id)->first();
        // Verificar se tem o jogo se n vai para a tela da listagem
        if(!empty($jogos)){
            return view('jogos.edit', ['jogos'=>$jogos]);
        }else{
            return redirect()->route('jogos-index');
        }
    }

    public function update(Request $request, $id){
        $data = [
        'nome' => $request->nome,
        'categoria' => $request->categoria,
        'ano_criacao' => $request->ano_criacao,
        'valor' => $request->valor,
        ];
  
        Jogo::where('id',$id)->update($data);

        return redirect()->route('jogos-index');
    }
```