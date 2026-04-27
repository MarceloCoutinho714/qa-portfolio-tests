## Fluxo Alternativo

### TC - POST - Login com e-mail em formato inválido
**ID:** API_POST_LOGIN_001

**Título:**  Validar login com e-mail em formato inválido

**Método:** POST

**Endpoint:** /login

### Regra de Negócio 

O sistema deve permitir o login do usuário apenas quando as credenciais informadas (e-mail e 
senha) forem válidas, estiverem cadastradas na base de dados e no formato esperado. Caso 
contrário, o acesso deve ser negado, retornando mensagens de erro claras e status HTTP 
apropriado.

### Pré-condição
Usuário possuir cadastro válido no sistema

### Passos
1. Enviar request POST para o endpoint de login <br>
2. Informar um e-mail em formato inválido <br>
Exemplo: usuarioemail.com <br>
3. Informar uma senha válida <br>
4. Executar a request <br><br>

### Resultado Esperado 
Status code **400**

O sistema não deve permitir o login

Deve exibir mensagem informando e-mail inválido

Nenhum token de autenticação deve ser gerado

### Resultado Obtido
Status code **400**

Login não realizado

Mensagem exibida: **“E-mail deve ser um e-mail válido”**

**Status:** PASS <br><br>

### TC -  POST - Login com senha inválida
**ID:** API_POST_LOGIN_002

**Título:**   Validar login com senha em formato inválido

**Método:** POST

**Endpoint:** /login

### Regra de Negócio 

O sistema deve permitir o login do usuário apenas quando as credenciais informadas (e-mail e 
senha) forem válidas, estiverem cadastradas na base de dados e no formato esperado. Caso 
contrário, o acesso deve ser negado, retornando mensagens de erro claras e status HTTP 
apropriado.

### Passos
1. Enviar request POST para o endpoint de login <br>
2. Informar um e-mail válido <br>
3. Informar uma senha inválida <br>
4. Executar a request <br>

### Resultado Esperado 
Status code **400**

O sistema não deve permitir o login

Deve exibir mensagem de credenciais inválidas

### Resultado Obtido
Status code **400**

Login não realizado

Mensagem exibida: “E-mail ou senha inválidos”

**Status:** PASS <br><br>


### TC - POST - Login sem preencher o campo e-mail
**ID:**  API_POST_LOGIN_003

**Título:** Validar login sem preenchimento do e-mail

**Método:** POST

**Endpoint:** /login

### Regra de Negócio 

O sistema deve permitir o login do usuário apenas quando as credenciais informadas (e-mail e 
senha) forem válidas, estiverem cadastradas na base de dados e no formato esperado. Caso 
contrário, o acesso deve ser negado, retornando mensagens de erro claras e status HTTP 
apropriado.

### Passos
1. Enviar request POST para o endpoint de login <br>
2. Não informar o campo e-mail <br>
3. Informar uma senha válida <br>
4. Executar a request <br>

### Resultado Esperado 
Status code **400**

O sistema não deve permitir o login

Deve validar campos obrigatórios

Deve exibir mensagem informando que o e-mail é obrigatório

### Resultado Obtido
Status code **400**

Login não realizado

Mensagem exibida: **“E-mail não pode ficar em branco”**

**Status:** PASS <br><br>

### TC - POST - Login sem preencher o campo senha
**ID:**  API_POST_LOGIN_004

**Título:**  Validar login sem preenchimento da senha

**Método:** POST

**Endpoint:**  /login

### Regra de Negócio 

O sistema deve permitir o login do usuário apenas quando as credenciais informadas (e-mail e 
senha) forem válidas, estiverem cadastradas na base de dados e no formato esperado. Caso 
contrário, o acesso deve ser negado, retornando mensagens de erro claras e status HTTP 
apropriado.

### Passos
1. Enviar request POST para o endpoint de login <br>
2. Informar um e-mail válido <br>
3. Não informar o campo senha <br>
4. Executar a request <br>

### Resultado Esperado 
Status code **400**

O sistema não deve permitir o login

Deve validar campos obrigatórios

Deve exibir mensagem informando que a senha é obrigatória

### Resultado Obtido
Status code **400**

Login não realizado

Mensagem exibida: **“Senha não pode ficar em branco”**

**Status:** PASS <br><br>




