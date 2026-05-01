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
“name” : “   ”, <br>
“e-mail” “nicole@gmail.com”, <br>
“password” :  “1234”, <br>
} <br>


### Resultado Esperado 
Status code **400**

O sistema não deve permitir o cadastro 

Deve exibir uma mensagem de erro informando que o campo **Nome é obrigatório.**

### Resultado Obtido
Status code **400**

Mensagem de erro obtida **“Nome é obrigatório”.**

**Status:** Pass <br><br>
## Evidência
![Tentativa de POST de usuário sem o nome](../evidencias/Erro/TC03_POST_001_Usuario_sem_nome.png)<br><br>

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

Mensagem de erro exibida **“E-mail não pode ficar em branco”**

**Status:** Pass <br><br>
## Evidência
![Tentativa POST de usuário sem e-mail](../evidencias/Erro/TC03_POST_002_Usuario_sem_e-mail.png)<br><br>

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

**Status:** Fail <br><br>

**Bug Relacionado:** BUG02 - API permite cadastro com senha composta apenas por espaço em branco.md <br>

**Severidade**<br>
Alta <br>

**Prioridade** <br>
Alta <br>


## Evidência
![Tentativa de POST com ausência de senha](../evidencias/Erro/BUG02_POST_Usuario_senha_invalida_apenas_espacos_bug.png)<br><br>

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
Status code **400**

O sistema não deve permitir o cadastro 

O campo nome deve aceitar apenas caracteres alfabéticos

Deve exibir mensagem de erro de validação

### Resultado Obtido
Status code **201**

Sistema permitiu o cadastro com números no campo nome 

Cadastro criado com sucesso 

ID gerado 

**Status:** Fail <br>

### Observação
O sistema não valida corretamente o tipo de dado do campo nome, permitindo caracteres 
inválidos, **ver com o time se tal comportamento é aceitável.** <br>

**Bug relacionado:**      <br>

**Severidade** <br>
Média <br>

**Prioridade** <br>
Média <br>

## Evidência
![Cadastro aprovado com números no campo nome](../evidencias/Erro/TC03_POST_003_Usuario_com_numeros_no_campo_nome.png)<br><br>

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
![Tentativa de cadastro de usuário com e-mail em formato inválido](../evidencias/Erro/TC03_POST_004_Usuario_com_e-mail_com_formato_invalido.png)

