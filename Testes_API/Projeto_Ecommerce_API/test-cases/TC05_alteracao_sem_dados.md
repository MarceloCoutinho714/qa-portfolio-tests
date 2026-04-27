## Fluxo Alternativo

### TC - PUT - Não Colocar Nome
**ID:** API_PUT_PROD_001

**Título:**  Validar erro ao alterar produto sem informar o nome

**Método:** PUT

**Endpoint:** /produtos/ { Id }

### Regra de Negócio 

O sistema deve permitir a alteração de produtos apenas quando os campos obrigatórios 
estiverem preenchidos.

### Passos
1. Enviar request PUT sem o campo nome.

### Input (body)
{<br>
"title": "  ",<br>
"price": 5000 ,<br>
"description": " Descrição ",<br>
"quantity": 35,<br>
"Id": 13,<br>
}<br>

### Resultado Esperado 
Status code **400**

Retornar mensagem de erro solicitando o nome

Produto não deve ser alterado

### Resultado Obtido
Status code **400**

Sistema retornou a mensagem de **“ nome é obrigatório “** e alteração não foi realizada


**Status:** PASS <br><br>

### TC - PUT - Não Colocar Preço
**ID:** API_PUT_PROD_002

**Título:**  Validar erro ao alterar produto sem informar o preço

**Método:** PUT

**Endpoint:** /produtos/ { Id }

### Regra de Negócio 

O sistema deve permitir a alteração de produtos apenas quando os campos obrigatórios 
estiverem preenchidos.

### Passos
1. Enviar request PUT sem o campo preço.

### Input (body)
{<br>
"title": "Tv 4K LG ",<br>
"price":  ,<br>
"description": " TV ",<br>
"quantity": 35,<br>
"Id": 13,<br>
}<br>

### Resultado Esperado 
Status code **400**

Retornar mensagem de erro solicitando o preço

Produto não deve ser alterado

### Resultado Obtido
Status code **400**

Sistema retornou a mensagem de **“ preço é obrigatório “** e alteração não foi realizada


**Status:** PASS <br><br>

### TC - PUT - Não Colocar Descrição
**ID:**  API_PUT_PROD_003

**Título:**  Validar erro ao alterar produto sem informar a descrição

**Método:** PUT

**Endpoint:** /produtos/ { Id }

### Regra de Negócio 

O sistema deve permitir a alteração de produtos apenas quando os campos obrigatórios 
estiverem preenchidos.

### Passos
1. Enviar request PUT sem o campo descrição.

### Input (body)
{<br>
"title": "Tv 4K LG ",<br>
"price": 2500 ,<br>
"description": "  ",<br>
"quantity": 35,<br>
"Id": 13,<br>
}<br>


### Resultado Esperado 
Status code **400**

Retornar mensagem de erro solicitando a descrição

Produto não deve ser alterado

### Resultado Obtido
Status code **400**

Sistema retornou a mensagem de **“ descrição é obrigatória “** e alteração não foi realizada


**Status:** PASS <br><br>


### TC - PUT - Não Colocar Quantidade
**ID:**  API_PUT_PROD_004

**Título:**  Validar erro ao alterar produto sem informar a quantidade

**Método:** PUT

**Endpoint:** /produtos/ { Id }

### Regra de Negócio 

O sistema deve permitir a alteração de produtos apenas quando os campos obrigatórios 
estiverem preenchidos.

### Passos
1. Enviar request PUT sem o campo quantidade.

### Input (body)
{<br>
"title": "Tv 4K LG ",<br>
"price": 2500 ,<br>
"description": " TV ",<br>
"quantity": ,<br>
"Id": 13,<br>
}<br>

### Resultado Esperado 
Status code **400**

Retornar mensagem de erro solicitando a quantidade

Produto não deve ser alterado

### Resultado Obtido
Status code **400**

Sistema retornou a mensagem de **“ quantidade é obrigatória “** e alteração não foi realizada


**Status:** PASS <br><br>




