
# Sistema: E-commerce API <br>

**Ferramenta:** Postman <br>

**Tipo de teste:** Funcional - API <br><br>

**Fluxo Principal** <br><br>

### TC01- POST- Criar Usuário <br>

**ID:** API_POST_USER_001 <br>

**Título:** Validar criação de usuário com dados válidos <br>

**Método:** POST <br>

**Endpoint:** /usuarios <br><br>

### Regra de Negócio <br>

O sistema deve permitir a criação de usuários quando os dados obrigatórios forem informados. <br>

### Passos <br>

1. Enviar request POST com dados válidos do usuário <br>

### Input (body)
{<br>
“name” : “ Fulano da Silva ”,<br>
“e-mail” “novousuario@qa.com”,<br>
“password” :  “teste”,<br>
"Admin": "true" ou "false" <br>
}<br>


### Resultado Esperado 

Status code **201**

Usuário criado com sucesso <br>

### Resultado Obtido 

Status code **201**

Usuário criado com sucesso 

**Status:** Pass <br><br>

## Evidência <br>
### Cadastro com Sucesso
![Cadastro de usuário realizado com sucesso.](../../evidencias/positivo/tc01-post-usuario-sucesso.png) <br><br>


### TC02 - POST - Login

**ID:** API_POST_LOGIN_001 <br>

**Título:** Validar login com credenciais válidas

**Método:** POST

**Endpoint:** /login

### Regra de Negócio
O sistema deve autenticar o usuário quando as credenciais forem válidas. <br>

### Passos

1. Enviar request POST com e-mail e senha válidos <br>

### Input (body)
{<br>
“e-mail”: “nicole@gmail.com”,<br>
“password” :  “1234”,<br>
}<br>

### Resultado Esperado 
Status code **200**

Retorna o Token de autenticação <br>

### Resultado Obtido 
Status code **200**

Token de autenticação gerado com sucesso

**Status:** Pass <br><br>

## Evidência
### Login com Sucesso
![Login realizado com sucesso.](../../evidencias/positivo/tc01-post-login-sucesso.png) <br><br>

### TC03 - GET - Lista de produtos

**ID:** API_GET_PROD_001

**Título:** Validar listagem de produtos cadastrados

**Método:** GET

**Endpoint:** /produtos

### Regra de Negócio 

O sistema deve retornar a lista de produtos cadastrados quando a request for válida. <br>

### Pré-condições 

* API disponível
* Existirem produtos cadastrados
  
### Passos

1. Enviar uma request GET para o endpoint /produtos

### Resultado Esperado 

Status code **200**

Retornar lista de produtos em formato JSON

Cada produto deve conter:

Nome <br>
Preço <br>
Descrição <br>
Quantidade <br>
id <br>

### Resultado Obtido

Status code **200**

Lista retornada corretamente.

**Status:** Pass <br><br>

## Evidência <br>
### Listagem de Produtos com Sucesso
![Listagem de Produtos com Sucesso.](../../evidencias/positivo/tc01-get-produtos-sucesso.png) <br><br>

### TC04 - POST - Cadastrar Produto

**ID:** API_POST_PROD_001

**Título:** Validar cadastro de novo produto com dados válidos 

**Método:** POST

**Endpoint:** /produtos 

### Regra de Negócio

O sistema deve permitir o cadastro de produtos quando todos os campos obrigatórios forem 
informados corretamente. 

### Pré-condições 

* Usuário autenticado 
* Token válido

### Passos

1. Enviar request POST com dados válidos do produto

### Input (body)
{<br>
"title": "Teclado DELL L250",<br>
"price": 120,<br>
"description": "Teclado silencioso",<br>
"quantity" : 100 ,<br>
}<br>

### Resultado Esperado

Status code **201**

Produto criado com sucesso 

Retornar ID do produto criado

### Resultado Obtido

Status code **201**

Produto cadastrado conforme esperado.

**Status:** Pass <br><br>

## Evidência
### Cadastro de Produto com Sucesso
![Cadastro de produto realizado com sucesso.](../../evidencias/positivo/tc01-post-produto-cadastrado-sucesso.png) <br><br>

### TC05 - DELETE - Deletar Produto
**ID:** API_DEL_PROD_001

**Título:** Validar exclusão de produto existente

**Método:** DELETE

**Endpoint:** /produtos/ { id }

### Regra de Negócio
O sistema deve permitir a exclusão de um produto existente quando o ID informado for válido.

### Pré-condições

* Produto existente 
* Usuário autenticado

### Passos 

Enviar uma request DELETE informando o ID do produto.

### Resultado Esperado

Status code **200**

Produto removido com sucesso 

### Resultado Obtido

Status code **200**

Produto deletado conforme esperado 

**Status:** Pass <br><br>

## Evidência
### Deletar Produto com Sucesso
![Produto deletado com sucesso.](../../evidencias/positivo/tc01-delete-produtos-sucesso.png) <br><br>





