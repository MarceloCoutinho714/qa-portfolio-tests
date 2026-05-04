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

Testes_Manuais/ <br>
|------ TC01_Registro_de_Usuario.md <br>
|------ TC02_Login_de_Usuario.md <br>
|------ TC03_Busca_de_Produtos.md <br>
|------ TC04_Carrinho.md <br>

---

Testes_API/ <br>

├── collections/ <br>
    └── Projeto_ServeRest_API.json <br>

├── environments/ <br>
    └── { <br>
  "base_url": "https://serverest.dev" <br>
}<br>

test-cases/ <br>
   ├── usuarios/ <br>
   ├── TC01_Fluxo_Principal.md <br>
   ├── TC03_POST_Usuario_com_ausencia_de_dados_obrigatorios.md <br>
   └── TC06_POST_Login_sem_dados_obrigatorios.md <br>

└── produtos/ <br>
    ├── TC02_POST_Produto_com_ausencia_de_dados_obrigatorios.md <br>
    ├── TC04_PUT_Alteracao_de_produto_com_id_inexistente.md <br>
    └── TC05_PUT_Alteracao_de_produto_sem_dados_obrigatorios.md <br>

├── bugs/ <br>
    ├── BUG01_PUT_faz_papel_de_POST_criando_um_novo_produto_aprovando_id_inexistente.md <br>
    ├── BUG02 _POST_API_permite_cadastro_com_senha_composta_apenas_por_espaço_em_branco.md <br>
    ├── BUG03_POST_API_permite_cadastro_com_nome_composto_apenas_por_espacos.md <br>
    
├── evidencias/ <br>
    ├── positivo/ # Fluxos válidos (testes que passaram)
    ├── negativo/ # Fluxos inválidos e cenários com falha/bug

└── README.md <br>

---

##  Objetivo Profissional
Este repositório faz parte do meu desenvolvimento na área de **Quality Assurance (QA)**, com foco em boas práticas de teste, organização de cenários e documentação clara para times de desenvolvimento.

---

##  Contato
- GitHub: https://github.com/MarceloCoutinho714
