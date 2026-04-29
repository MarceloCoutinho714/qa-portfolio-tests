### ID do BUG: BUG01_Criação_Aprovada_Pelo_Sistema
Título: Sistema permite cadastro com números e símbolos nos campos "Nome" e "Sobrenome" <br><br>

Tipo: BUG Funcional <br>
Ferramenta usada: Teste Manual (Navegador) <br>
Módulo: Cadastro de Usuário <br>
Tipo de teste: Teste Funcional Manual <br><br>

**Ambiente** <br>

Ambiente: Aplicação web de testes <br>
Ferramenta: Navegador (edge) <br>
Data do teste: 20/03/2026 <br><br>

**Pré-condição** <br>

Usuário acessar a página de cadastro do site. <br><br>

**Passos para Reproduzir** <br>

1. Acessar a página de cadastro. <br>

2. No campo "Nome", inserir números e/ou símbolos (exemplo: 123 ou João@). <br>

3. Preencher os demais campos obrigatórios corretamente. <br>

4. Clicar em "Cadastrar". <br><br>

**Resultado Esperado** <br>
O sistema deveria validar os campos "Nome" e "Sobrenome" e exibir mensagem informando que apenas letras são permitidas. <br>

**Resultado Obtido** <br>
O sistema permitiu a criação do cadastro utilizando números e símbolos nos campos "Nome" e "Sobrenome". <br>

**Observação Adicional** <br>
Campos de identificação do usuário normalmente possuem regras de validação para garantir a integridade dos dados cadastrados.
A ausência dessa validação pode permitir o registro de dados inconsistentes no sistema e impactar processos que dependem dessas informações. <br>

**Severidade** <br>
Média <br><br>

## Evidência <br>
**BUG** <br>
![Sistema aprova criação de cadastro com números no lugar do nome no campo nome](../Evidências/TC01_REGISTRATION/Cadastro-de-Usuario-com-Numeros-BUG.png) <br>
![Prova da criação do cadastro aprovada pelo sistema](../Evidências/TC01_REGISTRATION/Criacao-Aprovada-pelo-Sistema-BUG.png) <br>

