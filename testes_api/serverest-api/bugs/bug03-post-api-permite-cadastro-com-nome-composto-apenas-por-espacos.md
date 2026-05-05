**Origem:** TC03_POST_Usuario_com_ausencia_de_dados_obrigatorios.md <br>

### ID do Bug: BUG03_POST_API_permite_cadastro_com_nome_composto_apenas_por_espacos
Título: POST em /usuarios permite cadastro com nome composto apenas por espaços em branco. <br><br>

Tipo: BUG Funcional API <br>
Ferramenta usada: Postman <br>
API Endpoint: /usuarios <br>
Método HTTP: POST <br>
Tipo de teste: Negativo API Test <br><br>

### Ambiente

Ambiente: API pública de testes <br>
Ferramenta: Postman <br>
Data do teste: 01/05/2026<br>

### Pré-condição

API disponível e funcional. <br>

### Passos para Reproduzir
1. Enviar uma requisição POST para o endpoint /usuarios.<br>
2. Informar um e-mail válido.<br>
3. Definir o campo "nome" como " " (apenas espaços em branco).<br>
4. Informar uma senha válida.<br>
5. Executar a request.<br><br>

### Resultado Esperado

A API deveria validar o campo nome e rejeitar valores compostos apenas por espaços em branco.

Status Code: 400 (Bad Request)

Mensagem de erro indicando que o campo nome é obrigatório ou inválido. <br><br>

### Resultado Obtido

A API permitiu o cadastro do usuário e retornou Status Code: 201 (Created)

Mensagem: "Cadastro realizado com sucesso"

Isso indica falha na validação do campo nome, permitindo entrada inválida.<br><br>

### Observação Adicional

Foi identificado comportamento inconsistente na validação do campo nome

Quando o campo "nome" é enviado vazio (""), a API retorna corretamente erro 400 (Bad Request)

Porém, quando o campo é enviado com apenas espaços (" "), a API aceita a requisição e realiza o cadastro normalmente 201 (Created)

Esse comportamento indica ausência de tratamento de espaços em branco (trim) antes da validação.<br><br>

**Severidade** <br>
Média

**Prioridade** <br>
Média <br><br>

Evidência <br>
![Cadastro com espaços no campo nome aceito pelo sistema](../evidencias/negativo/bug03-post-api-permite-cadastro-com-nome-composto-apenas-por-espacos.png)<br>
