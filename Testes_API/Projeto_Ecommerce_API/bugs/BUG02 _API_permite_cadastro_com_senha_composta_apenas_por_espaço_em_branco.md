**Origem:** TC03_POST_usuario_com_ausencia_de_dados_obrigatorios.md
### ID do Bug: BUG02_API_permite_cadastro_com_senha_composta_apenas_por_espaço_em_branco <br>

Título: POST em /usuarios permite cadastro com senha composta apenas por espaço em branco. <br><br>

Tipo: BUG Funcional API <br>
Ferramenta usada: Postman <br>
API Endpoint: /usuarios <br>
Método HTTP: POST <br>
Tipo de teste: Negativo API Test <br><br>

### Ambiente
Ambiente: API pública de testes <br>
Ferramenta: Postman<br>
Data do teste: 30/04/2026<br>

### Pré-condição 

API disponível e funcional. <br>

### Passos para Reproduzir 

1. Enviar uma requisição POST para o endpoint /usuarios.<br>

2. Informar dados válidos para nome e email.<br>

3. Definir o campo "password" como `" "` (um espaço em branco).<br>

4. Executar a request.<br>

### Resultado Esperado 

A API deveria validar o campo senha e rejeitar valores compostos apenas por espaço em branco.

Status Code: **400 (Bad Request)**

Mensagem de erro indicando senha inválida ou obrigatória. <br><br>

### Resultado Obtido

A API permitiu o cadastro do usuário e retornou:

Status Code: **201 (Created)**

Mensagem: "Cadastro realizado com sucesso"

Isso indica falha na validação do campo senha, permitindo entrada inválida.<br><br>

### Observação Adicional 

Foi observado comportamento inconsistente na validação do campo senha:

Quando o campo "password" é enviado vazio (`""`), a API retorna corretamente erro **400 (Bad Request)**.<br>

Porém, quando o campo é enviado com um espaço em branco (`" "`), a API aceita a requisição e realiza o cadastro normalmente.<br><br>

**Severidade** <br>
Alta

**Prioridade** <br>
Alta <br><br>

### Evidência <br>
![POST usuario aceita senha com espaço](../evidencias/erro/)<br>
