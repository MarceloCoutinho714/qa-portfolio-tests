## Fluxo Alternativo

### TC01 - POST - Não Colocar Nome
**ID:** API_POST_PROD_002

**Título:** Validar erro ao cadastrar produto sem nome

**Método:** POST

**Endpoint:** /produtos

### Regra de Negócio 

O sistema não deve permitir o cadastro de produtos sem informar os campos obrigatórios.

### Passos
1. Enviar request POST sem o campo nome.

### Input (body)
{ <br>
"title": "  ",<br>
"price": 100,<br>
"description": "A description",<br>
"quantity": 58,<br>
} <br>

### Resultado Esperado 
Status code **400**

Retornar mensagem de erro solicitando o nome

Produto não deve ser cadastrado 

### Resultado Obtido
Status code **400**

Sistema retornou a mensagem de “ nome é obrigatório “ e cadastro não foi realizado

**Status:** Pass <br><br>

## Evidência
![POST Tentativa de cadastro de porduto sem nome](../../evidencias/negativo/TC02_POST_002_Produto_sem_nome.png)<br><br>

### TC02 - POST - Não Colocar Preço
**ID:** API_POST_PROD_003

**Título:** Validar erro ao cadastrar produto sem preço

**Método:** POST

**Endpoint:** /produtos

### Regra de Negócio 
O sistema não deve permitir o cadastro de produtos sem informar os campos obrigatórios.

### Passos
1. Enviar request POST sem o campo preço.

### Input (body)
{ <br>
"title": " Teclado sem fio ",<br>
"price":   ,<br>
"description": "Teclado",<br>
"quantity": 58,<br>
} <br>

### Resultado Esperado 
Status code **400**

Retornar mensagem de erro solicitando o preço

Produto não deve ser cadastrado 

### Resultado Obtido
Status code **400**

Sistema retornou a mensagem de “ preço é obrigatório “ e cadastro não foi realizado

**Status:** Pass <br><br>

## Evidência
![POST Tentativa de cadastrar produto sem o preço](../../evidencias/negativo/TC02_POST_001_Produto_sem_preco.png)<br><br>

### TC03 - POST - Não Colocar Descrição
**ID:** API_POST_PROD_004

**Título:** Validar erro ao cadastrar produto sem descrição

**Método:** POST

**Endpoint:** /produtos

### Regra de Negócio 
O sistema não deve permitir o cadastro de produtos sem informar os campos obrigatórios.

### Passos
1. Enviar request POST sem o campo descrição.

### Input (body)
{ <br>
"title": " Teclado sem fio ",<br>
"price": 250,<br>
"description": "   ",<br>
"quantity": 58,<br>
} <br>

### Resultado Esperado 
Status code **400**

Retornar mensagem de erro solicitando descrição

Produto não deve ser cadastrado 

### Resultado Obtido
Status code **400** 

Sistema retornou a mensagem de “ descrição é obrigatória “ e cadastro não foi realizado

**Status:** Pass <br><br>
## Evidência
![POST Tentativa de cadastrar produto sem a descrição](../../evidencias/negativo/TC02_POST_003_Produto_sem_decricao.png)<br><br>

### TC04 - POST - Não Colocar Quantidade
**ID:** API_POST_PROD_005

**Título:** Validar erro ao cadastrar produto sem quantidade

**Método:** POST

**Endpoint:** /produtos

### Regra de Negócio 
O sistema não deve permitir o cadastro de produtos sem informar os campos obrigatórios.

### Passos
1. Enviar request POST sem o campo quantidade.

### Input (body)
{ <br>
"title": " Teclado sem fio ",<br>
"price": 250,<br>
"description": " Teclado ",<br>
"quantity":  ,<br>
} <br>


### Resultado Esperado 
Status code **400**

Retornar mensagem de erro solicitando quantidade

Produto não deve ser cadastrado 

### Resultado Obtido
Status code **400**

Sistema retornou a mensagem de “ quantidade é obrigatória “ e cadastro não foi realizado

**Status:** Pass <br><br>
## Evidência
![POST Tentativa de cadastrar produto sem a quantidade](../../evidencias/negativo/TC02_POST_004_Produto_sem_quantidade.png)<br><br>
