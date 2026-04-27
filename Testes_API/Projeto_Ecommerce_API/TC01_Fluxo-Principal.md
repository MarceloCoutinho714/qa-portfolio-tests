Sistema: E-commerce (API)
Ferramenta: Postman
Tipo de teste: Funcional - API
Fluxo Principal
Test Case - POST- Criar Usuário 
ID: API_POST_USER_001
Título; Validar criação de usuário com dados válidos 
Método: POST
Endpoint: /usuarios
Regra de Negócio
O sistema deve permitir a criação de usuários quando os dados obrigatórios forem informados.
Passos
1. Enviar request POST com dados válidos do usuário 
Resultado Esperado 
Status code 201
Usuário criado com sucesso 
Status: Passou 
Test Case - POST - Login
ID: API_POST_LOGIN_001
Título: Validar login com credenciais válidas
Método: POST
Endpoint: /login
Regra de Negócio
O sistema deve autenticar o usuário quando as credenciais forem válidas.
Passos
1. Enviar request POST com login e senha válidos
Resultado Esperado 
Status code 200
Retorna o Token de autenticação 
Status: Passou 
Test case - GET - Lista de produtos
ID: API_GET_PROD_001
Título: Validar listagem de produtos cadastrados
Método: GET
Endpoint: /produtos
Regra de Negócio 
O sistema deve retornar a lista de produtos cadastrados quando a request for válida.
Pré-condições 
API disponível
Existirem produtos cadastrados 
Passos
1. Enviar uma request GET para o endpoint /produtos 
Resultado Esperado 
Status code 200
Retornar lista de produtos em formato JSON
Cada produto deve conter:
Nome
Preço
Descrição
Quantidade
id
Resultado Obtido
Lista retornada corretamente.
Status: Passou
Test Case - POST - Cadastrar Produto
ID: API_POST_PROD_001
Título: Validar cadastro de novo produto com dados válidos 
Método: POST
Endpoint: /produtos 
Regra de Negócio
O sistema deve permitir o cadastro de produtos quando todos os campos obrigatórios forem 
informados corretamente.
Pré-condições 
Usuário autenticado 
Token válido
Passos
1. Enviar request POST com dados válidos do produto
Resultado Esperado
Status code 201
Produto criado com sucesso 
Retornar ID do produto criado
Resultado Obtido
Produto cadastrado conforme esperado.
Status: Passou
Test Case - DELETE - Deletar Produto
ID: API_DEL_PROD_001
Título: Validar exclusão de produto existente
Método: DELETE
Endpoint: /produtos/ { id }
Regra de Negócio
O sistema deve permitir a exclusão de um produto existente quando o ID informado for válido.
Pré-condições
Produto existente 
Usuário autenticado 
Passos 
Enviar uma request DELETE informando o ID do produto
Resultado Esperado
Status code 200
Produto removido com sucesso 
Resultado Obtido
Produto deletado conforme esperado 
Status: Passo
