# Bug ID: API-BUG-001 <br>

Título: PUT em /produtos/{id} cria novo produto ao usar ID inexistente. <br><br>

Tipo: BUG Funcional API <br>
Ferramenta usada: Postman <br>
API Endpoint: /produtos/{id} <br>
Método HTTP: PUT <br>
Tipo de teste: Negativo API Test <br><br>

### Ambiente
Ambiente: API pública de testes <br>
Ferramenta: Postman<br>
Data do teste: 31/01/2026<br>

### Pré-condição 

Nenhum produto existente com o ID informado na requisição. <br>

### Passos para Reproduzir 

1. Criar um ID aleatório inexistente (não presente na base da API).

2. Enviar uma requisição PUT para o endpoint /produtos/{id} utilizando esse ID inexistente.

3. Informar dados válidos de produto no body da requisição.

4. Executar a request.

### Resultado Esperado 

A API deveria retornar erro indicando que o recurso não existe.

Status Code: **404**

Sem criação de um novo produto.

### Resultado Obtido

A API criou um novo produto e retornou:

Status Code: **201 (Created)**

Além disso, a API gerou um novo ID automaticamente, ignorando o ID informado na requisição.

Isso indica quebra de contrato da API, pois o método PUT deveria atualizar um recurso existente e não criar um novo.

### Observação Adicional 

O teste foi realizado utilizando um ID gerado manualmente e de forma aleatória, garantindo que o recurso não existia previamente na API.

Mesmo assim, o sistema criou um novo produto em vez de retornar erro apropriado.

### Severidade
Média

### Prioridade
Média

## Evidência <br>
![PUT faz papel de POST e cria um novo produto](evidencias/put_produto_cria_em_vez_de_atualizar_bug.png)<br>



