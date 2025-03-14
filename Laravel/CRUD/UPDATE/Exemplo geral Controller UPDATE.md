```php
    public function edit($id){
        $variavel = NomeController::where('id', $id)->first();
        // Verificar se tem o jogo se n vai para a tela da listagem
        if(!empty($variavel)){
            return view('caminho.arquivo', ['OqueÉ'=>$variavel]);
        }else{
            return redirect()->route('NomeDaRotaDeListagem');
        }
    }

    public function update(Request $request, $id){
        $data = [
        //Mesmos nomes das colunas do Banco
        'OqueVaiMudar01' => $request->OqueVaiMudar01,
        'OqueVaiMudar02' => $request->OqueVaiMudar02,
        'OqueVaiMudar03' => $request->OqueVaiMudar03,
        'OqueVaiMudar04' => $request->OqueVaiMudar04,
        ];
  
        NomeController::where('id',$id)->update($variavel);

        return redirect()->route('NomeDaRotaDeListagem');
    }
```