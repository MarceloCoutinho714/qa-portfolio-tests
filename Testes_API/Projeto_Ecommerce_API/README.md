#  Testes de API - Projeto SERVEREST E-commerce

##  Descrição
Este projeto contém testes de API realizados em um sistema de e-commerce, com foco na validação dos principais fluxos de usuário e operações de CRUD.

---

##  Objetivo
- Validar o funcionamento dos endpoints da API  
- Garantir integridade dos dados  
- Testar fluxos principais e alternativos  
- Identificar possíveis falhas  

---

##  Fluxo Principal

Os seguintes cenários foram testados:

1. Criação de usuário (**POST**)  
2. Login do usuário (**POST**)  
3. Listagem de produtos (**GET**)  
4. Cadastro de produto (**POST**)  
5. Exclusão de produto (**DELETE**)  

---

##  Fluxos Alternativos

Também foram testados cenários de erro e validação, como:

- Dados inválidos no cadastro  
- Falha de autenticação no login  
- Tentativas de acesso não autorizado  
- Validações de campos obrigatórios  

---

## Estrutura do Projeto

 Testes_API/ <br>
 └── Projeto_Ecommerce_API/<br>
    └──  bugs/<br>
    
    ├── BUG01_put_produto_atualizacao.md<br>
    
  └──  evidencias/<br>
    
    └── sucesso<br>
    ├──  delete_produtos_sucesso.png<br>
    ├──  get_produtos_sucesso.png<br>
    ├──  post_login_sucesso.png<br>
    ├──  post_produtos_sucesso.png<br>
    ├──  post_usuario_sucesso.png<br>
    
    └──  erro<br>
    ├──  put_produto_duplicado.png<br>
    ├──  put_produto_dados_ausentes.png<br>
    
 └── test-cases/<br>
  
    ├──  TC01_fluxo_principal.md<br>
    ├──  TC02_produto_sem_dados.md<br>
    ├──  TC03_usuario_sem_dados.md<br>
    ├──  TC04_alteracao_id_inexistente.md<br>
    ├──  TC05_alteracao_sem_dados.md<br>
    ├──  TC06_login_sem_dados.md<br>
    ├──  README.md<br>
 └──README.md<br>




