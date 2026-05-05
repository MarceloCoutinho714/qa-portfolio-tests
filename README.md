# QA-Portfólio-Tests

##  Sobre o Projeto
Este repositório tem como objetivo apresentar um portfólio de **testes manuais** e **testes de API em QA**, focado na validação funcional de sistemas e regras de negócio.

Os testes documentados simulam cenários reais de aplicações web, com foco em qualidade, clareza e organização. 

---

##  Tipos de Testes Abordados
- Testes funcionais
- Testes de validação de campos
- Testes de busca e filtros
- Testes de login
- Testes de API 

---

##  Ferramentas Utilizadas
- Testes manuais
- Documentação de casos de teste
- Postman (para testes de API)
- GitHub para versionamento e portfólio

---

##  Estrutura do Repositório

testes_manuais/ <br>
├── tc01-registro-de-usuario.md <br>
├── tc02-login-de-usuario.md <br>
├── tc03-busca-de-produtos.md <br>
└── tc04-carrinho.md <br>

bugs/<br>
└── bug01-login-com-tentativas-ilimitadas.md <br>

evidencias/ <br>
 ├── positivo/ # Fluxos válidos (testes que passaram) <br>
 └── negativo/ # Fluxos inválidos e cenários com falha/bug <br>

└── README.md <br>
 
---

testes_api/ <br>

├── collections/ <br>
    └── serverest-api.json <br>

├── environments/ <br>
    └── { <br>
  "base_url": "https://serverest.dev" <br>
}<br>

test-cases/ <br>
   ├── usuarios/ <br>
   ├── tc01-fluxo-principal.md <br>
   ├── tc03-post-usuario-com-ausencia-de-dados-obrigatorios.md <br>
   └── tc06-post-login-sem-dados-obrigatorios.md <br>

└── produtos/ <br>
    ├── tc02-post-produto-com-ausencia-de-dados-obrigatorios.md <br>
    ├── tc04-put-alteracao-de-produto-com-id-inexistente.md <br>
    └── tc05-put-alteracao-de-produto-sem-dados-obrigatorios.md <br>

├── bugs/ <br>
    ├── bug01-put-faz-papel-de-post-criando-um-novo-produto-aprovando-id-inexistente.md <br>
    ├── bug02-api-permite-cadastro-com-senha-composta-apenas-por-espacos-em-branco.md <br>
    └── bug03-post-api-permite-cadastro-com-nome-composto-apenas-por-espacos.md <br>
    
├── evidencias/ <br>
    ├── positivo/ # Fluxos válidos (testes que passaram) <br>
    └── negativo/ # Fluxos inválidos e cenários com falha/bug <br>

└── README.md <br>

---

##  Objetivo Profissional
Este repositório faz parte do meu desenvolvimento na área de **Quality Assurance (QA)**, com foco em boas práticas de teste, organização de cenários e documentação clara para times de desenvolvimento.

---

##  Contato
- GitHub: https://github.com/MarceloCoutinho714
