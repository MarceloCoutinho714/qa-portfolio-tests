## Fluxo Alternativo

### TC01 - PUT - Alterar Produto Com ID Inexistente
**ID:** API_PUT_PROD_001

**Título:** Validação de erro para Id inexistente

**Método:** PUT

**Endpoint:** /produtos/ { Id }

### Regra de Negócio 

O sistema não deve permitir a alteração de produtos inexistentes.

### Passos
1. Enviar request PUT com um ID inexistente.

### input (body)
{<br>
"title": "TV 4K LG ",<br>
"price": 3000,<br>
"description": " Tv ",<br>
"Id": 12**5166@$&&@156,<br>
}<br>

### Resultado Esperado 
Status code **404**

O sistema não deve permitir a alteração de um produto inexistente 

Sistema deve exibir mensagem informando que o produto não foi localizado

### Resultado Obtido
Status code **201 - Created**

Sistema permitiu a operação 

Exibiu a mensagem **“ Cadastro realizado com sucesso “**

Um novo produto foi criado ignorando o ID inexistente informado na URL

### Observação
O método PUT está se comportando como POST, permitindo a criação de um novo produto ao 
invés de bloquear a alteração de um recurso inexistente.

Comportamento em desacordo com a regra de negócio e com o padrão REST.

**Status:** Fail <br>

**Bug relacionado:** BUG01_PUT_faz_papel_de_POST_criando_um_novo_produto_aprovando_id_inexistente.md

**Severidade:** <br>
Média <br>

**Prioriade:** <br>
Média <br>

## Evidência
![PUT fez papel de POST e cria um produto](../../evidencias/negativo/bug01-put-faz-papel-de-post-criando-um-novo-produto-aprovando-id-inexistente.png) <br><br>

**Bug identificado:** API permite PUT fazer papel de POST criando um novo produto ignorando ID inexistente.



