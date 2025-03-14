tag: #Laravel 

**5º Passo:** -> Dentro do método **up()**, use `$table->tipoDeDado('nomeDaColuna')` para definir as colunas da tabela. Você pode adicionar mais configurações, como tamanho ou atributos extras, se necessário.

```php
<?php
use Illuminate\Database\Migrations\Migration;

use Illuminate\Database\Schema\Blueprint;

use Illuminate\Support\Facades\Schema;


return new class extends Migration
{
    /**
     * Run the migrations.
     */
    public function up(): void
    {
        Schema::create('jogos', function (Blueprint $table) {
            $table->id();
            $table->string('nome',55);
            $table->string('categoria',55);
            // Caso queira um valor default
            $table->year('ano_criaçcao')->default('2021');
            $table->double('valor',8,2);
            $table->timestamps();
        });
    }
    /**
     * Reverse the migrations.
     */
    public function down(): void
    {
        Schema::dropIfExists('jogos');
    }
};
```

O `->default(2021)` isso foi utilizado para que se caso a pessoa não coloque o ano de criação o valor que será preenchido será o 2021. Um valor padrão.