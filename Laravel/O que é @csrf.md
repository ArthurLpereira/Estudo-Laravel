No Laravel, `@csrf` é um **token de proteção contra ataques CSRF** (Cross-Site Request Forgery).

Quando você usa um formulário com o método **POST**, o Laravel exige que você inclua esse token para garantir que a requisição veio do próprio site, não de um ataque externo.