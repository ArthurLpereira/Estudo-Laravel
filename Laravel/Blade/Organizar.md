tag: #Laravel 

Como deixar organizado dentro de views crie uma pasta com o nome do conteudo que deseja criar e dentro dela é onde terá a maior parte do código (index.blade.php no nosso exemplo), e depois crie uma de layouts que é onde será mostrado todo o código escrito (app.blade.php no nosso exemplo) na outra página.

```bash
resources
└── views
    ├── jogos
    │   └── index.blade.php
    └── layouts
        └── app.blade.php
```
