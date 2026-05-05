## Fluxo Alternativo

### TC01 - POST - Cadastrar Usuário sem Informar Nome
**ID:** API_POST_USER_001

**Título:** Validar cadastro sem preenchimento do campo nome

**Método:** POST

**Endpoint:** /usuarios

### Regra de Negócio 

O sistema deve permitir o cadastro de usuários apenas quando todos os campos obrigatórios 
estiverem preenchidos com dados válidos e no formato esperado.

### Passos
1. Deixar campo nome em branco.

### Input (body)
{ <br>
“name” : “”, <br>
“e-mail” “nicole@gmail.com”, <br>
“password” :  “1234”, <br>
} <br>


### Resultado Esperado 
Status code **400**

O sistema não deve permitir o cadastro 

Deve exibir uma mensagem de erro informando que o campo **Nome é obrigatório.**

### Resultado Obtido
O sistema apresentou comportamento inconsistente na validação do campo nome <br>

Quando o campo é enviado vazio (""), o cadastro é corretamente rejeitado com Status Code 400 <br>

Porém, quando o campo é preenchido apenas com espaços (" "), o sistema permite o cadastro e retorna Status Code 201 <br><br>

**Status:** Fail <br>

**Bug relacionado:** BUG03_POST_API_permite_cadastro_com_nome_composto_apenas_por_espacos.md <br>

**Severidade**<br>
Média<br>

**Prioridade**<br>
Média<br>


## Evidência
**Campo nome vazio**<br><br>
![Tentativa de POST de usuário sem o nome](../../evidencias/negativo/tc03-post-usuario-sem-nome.png)<br><br>
## Evidência
**Campo nome preenchido apenas com espaços**<br><br>
![Tentativa de POST de usuário sem o nome](../../evidencias/negativo/bug03-post-api-permite-cadastro-com-nome-composto-apenas-por-espacos.png)<br><br>

**Bug identificado:** API permite cadastro de produto com campo "nome" contendo apenas espaços em branco, indicando ausência de validação de entrada para campos obrigatórios. <br><br>

### TC02 - POST - Cadastrar Usuário sem Informar E-mail 
**ID:** API_POST_USER_002

**Título:**  Validar cadastro sem preenchimento do campo e-mail

**Método:** POST

**Endpoint:** /usuarios

### Regra de Negócio 
O sistema deve permitir o cadastro de usuários apenas quando todos os campos obrigatórios 
estiverem preenchidos com dados válidos e no formato esperado.

### Passos
1. Deixar campo e-mail em branco

### Input (body)
{ <br>
“name” : “ Nicole ”, <br>
“e-mail” “    ”, <br>
“password” : “1234”, <br>
} <br>

### Resultado Esperado 
Status code **400**

O sistema não deve permitir o cadastro 

Deve exibir uma mensagem de erro informando que o campo **E-mail é obrigatório.**

### Resultado Obtido
Status code **400**

Mensagem de erro exibida **“E-mail deve ser um e-mail válido”**

**Status:** Pass <br><br>
## Evidência
![Tentativa POST de usuário sem e-mail](../../evidencias/negativo/tc03-post-usuario-sem-email.png)<br><br>

### TC03 - POST - Cadastrar Usuário sem Informar Senha
**ID:**  API_POST_USER_003

**Título:** Validar cadastro sem preenchimento do campo senha

**Método:** POST

**Endpoint:** /usuarios

### Regra de Negócio 
O sistema deve permitir o cadastro de usuários apenas quando todos os campos obrigatórios 
estiverem preenchidos com dados válidos e no formato esperado.

### Passos
1. Deixar campo senha em branco

### Input (body)
{ <br>
“name” : “ Nicole ”, <br>
“e-mail” “ nicole@gmail.com ”, <br>
“password” : “”, <br>
} <br>

### Resultado Esperado 
Status code **400**

O sistema não deve permitir o cadastro 

Deve exibir uma mensagem de erro informando que o campo **Senha é obrigatório.**

### Resultado Obtido
Status code **201 - Created** <br>
Usuário cadastrado com sucesso <br>

**Status:** Fail <br>

**Bug Relacionado:** bug02-api-permite-cadastro-com-senha-composta-apenas-por-espacos-em-branco.md <br>

**Severidade**<br>
Alta <br>

**Prioridade** <br>
Alta <br>


## Evidência
![Tentativa de POST com ausência de senha](../../evidencias/negativo/bug02-api-permite-cadastro-com-senha-composta-apenas-por-espacos-em-branco.png)<br><br>

**Bug identificado:** API permite cadastro de produto com campo "senha" contendo apenas espaços em branco, indicando ausência de validação de entrada para campos obrigatórios. <br><br>

### TC04 - POST - Cadastro Informando Números no Campo Nome
**ID:**  API_POST_USER_004

**Título:** Validar cadastro com caracteres numéricos no campo nome

**Método:** POST

**Endpoint:** /usuarios

### Regra de Negócio 
O sistema deve permitir o cadastro de usuários apenas quando todos os campos obrigatórios 
estiverem preenchidos com dados válidos e no formato esperado.

### Passos
1. Preencher o campo **Nome** com números (ex:12345)

### Input (body)
{ <br>
“name” : “ 7712 ”, <br>
“e-mail” “ nicole@gmail.com ”, <br>
“password” : “1234”, <br>
} <br>

### Resultado Esperado 
O sistema deve aceitar string no campo nome

### Resultado Obtido
Status code **201**

Sistema permitiu o cadastro com números no campo nome 

Cadastro criado com sucesso 

ID gerado 

**Status:** Pass <br>

### Observação 
O campo nome aceita valores numéricos. Não há regra clara na API indicando restrição de formato. Validar com o time se esse comportamento é esperado.<br>

## Evidência
![Cadastro aprovado com números no campo nome](../../evidencias/negativo/tc03-post-usuario-com-numeros-no-campo-nome.png)<br><br>

### TC05 - POST- Cadastro com E-mail em Formato Inválido
**ID:**  API_POST_USER_005

**Título:** Validar cadastro com e-mail em formato inválido

**Método:** POST

**Endpoint:** /usuarios

### Regra de Negócio
O sistema deve permitir o cadastro de usuários apenas quando todos os campos obrigatórios 
estiverem preenchidos com dados válidos e no formato esperado.

### Passos
1. Preencher o campo E-mail com um valor em formato inválido (ex: mariasilva.com.br, 
mariasilva.br, mariasilva.com)

### Input (body)
{ <br>
“name” : “ Nicole ”, <br>
“e-mail” “ nicole.com ”, <br>
“password” : “1234”, <br>
} <br>

### Resultado Esperado 
Status code **400**

O sistema não deve permitir o cadastro 

Deve exibir uma mensagem de erro informando que o formato do e-mail é inválido 

### Resultado Obtido
Status code **400** 

Mensagem de erro obtida: **“E-mail deve ser um e-mail válido”.**

**Status:** Pass <br><br>

## Evidência
![Tentativa de cadastro de usuário com e-mail em formato inválido](../../evidencias/negativo/tc03-post-usuario-com-email-em-formato-errado.png)

