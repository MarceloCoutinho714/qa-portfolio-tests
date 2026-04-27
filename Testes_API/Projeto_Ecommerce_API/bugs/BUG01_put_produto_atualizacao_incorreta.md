Bug ID: API-BUG-002
Título: PUT em /produtos/{id} cria novo produto ao usar ID inexistente.

Tipo: BUG Funcional API
Ferramenta usada: Postman
API Endpoint: /produtos/{id}
Método HTTP: PUT
Tipo de teste: Negativo API Test

Ambiente
Ambiente: API pública de testes
Ferramenta: Postman
Data do teste: 31/01/2026

Pré-condição 

Nenhum produto existente com o ID informado na requisição.

Passos para Reproduzir 

Criar um ID aleatório inexistente (não presente na base da API).

Enviar uma requisição PUT para o endpoint /produtos/{id} utilizando esse ID inexistente.

Informar dados válidos de produto no body da requisição.

Executar a request.

Resultado Esperado 

A API deveria retornar erro indicando que o recurso não existe.

Status Code: 404 

Sem criação de um novo produto.

Resultado Obtido

A API criou um novo produto e retornou:

Status Code: 201 (Created)

Além disso, a API gerou um novo ID automaticamente, ignorando o ID informado na requisição.

Isso indica quebra de contrato da API, pois o método PUT deveria atualizar um recurso existente e não criar um novo.

Observação Adicional 

O teste foi realizado utilizando um ID gerado manualmente e de forma aleatória, garantindo que o recurso não existia previamente na API.

Mesmo assim, o sistema criou um novo produto em vez de retornar erro apropriado.

Severidade

Média

Prioridade

Média
