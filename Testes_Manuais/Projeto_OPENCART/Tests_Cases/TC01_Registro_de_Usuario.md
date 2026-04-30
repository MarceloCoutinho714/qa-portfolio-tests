## Feature: Cadastro de Usuário

Ambiente: Web/Edge/Windows

Pré-condição: Usuário acessar página inicial da Opencart<br>

### Test Data
Nome: Fernando (Formato válido Texto alfabético)    <br>
Sobrenome: Oliveira (Formato válido Texto alfabético)  <br>
E-mail: fernandoteste@gmail.com (Formato Válido)<br> 
Senha: Entrar1234* (mín. 4 caracteres, com maiúscula, número e símbolo)  <br>


Passos:
1. Clicar em minha conta 
2. Clicar em cadastrar
3. Inserir um nome válido no campo "Primeiro Nome" conforme Test Data
4. Inserir um sobrenome válido no campo “Sobrenome” conforme Test Data
5. Inserir um email válido conforme Test Data
6. Inserir uma senha válida conforme Test Data
7. Confirmar a senha no campo “Confirmar Senha”
8. Marcar o checkbox “Política de Privacidade”
9. Clicar no botão “Continue” <br><br><br>
**Regra de Negócio**

O sistema deve permitir a criação de uma conta apenas quando todos os campos obrigatórios 
(Nome, Sobrenome, E-mail e Senha) forem preenchidos com dados válidos, respeitando as 
regras de validação definidas para cada campo. <br><br>   

Testes Funcionais - Fluxo Principal <br><br>

**TC_001.** Inserir nome válido no campo "Nome" <br><br>
**Resultado esperado:** O sistema deve aceitar o nome inserido, não exibir mensagens de erro e permitir a continuidade do preenchimento do formulário de cadastro. <br>

**Resultado Obtido:** O sistema aceitou o nome inserido sem apresentar mensagens de erro e permitiu a continuidade do cadastro.<br>

**Status: PASS** <br><br>

### Evidência
![Nome válido](../Evidências/TC01_REGISTRATION/Sucesso/TC01_REGISTRATION_001_Nome_Valido.png)

**TC_002.** Inserir sobrenome válido no campo "Sobrenome" <br><br>

**Resultado esperado:** O sistema deve aceitar o sobrenome inserido, não exibir mensagens de erro e permitir a continuidade do cadastro.<br>

**Resultado Obtido:** O sistema aceitou o sobrenome inserido sem apresentar mensagens de erro e permitiu a continuidade do cadastro.<br>

**Status: PASS** <br><br>

### Evidência
![Sobrenome válido](../Evidências/TC01_REGISTRATION/Sucesso/TC01_REGISTRATION_002_Sobrenome_Valido.png)

**TC_003.** Inserir e-mail válido no campo "E-mail" <br>

**Resultado esperado:** O sistema deve aceitar o e-mail inserido no formato válido, não exibir mensagens de erro e permitir a continuidade do cadastro.<br>

**Resultado Obtido:** O sistema aceitou o e-mail inserido sem apresentar mensagens de erro e permitiu a continuidade do cadastro. <br>

**Status: PASS** <br><br>

### Evidência
![E-mail válido](../Evidências/TC01_REGISTRATION/Sucesso/TC01_REGISTRATION_003_E-mail_Valido.png)

**TC_004.** Inserir senha com caracteres válidos <br>

**Resultado esperado:** O sistema deve aceitar a senha inserida conforme os critérios mínimos definidos, não exibir mensagens de erro e permitir a conclusão do cadastro. <br>

**Resultado Obtido:** O sistema aceitou a senha inserida sem apresentar mensagens de erro e permitiu a conclusão do cadastro. <br>

**Status: PASS** <br><br>

### Evidência
![Senha em formato válido](../Evidências/TC01_REGISTRATION/Sucesso/TC01_REGISTRATION_012_Senha_Valida.png) <br><br>


Fluxo Alternativo <br><br>


**TC_005.** Deixar o campo "Nome" em branco <br>

**Resultado esperado:** O sistema deve impedir a continuidade do cadastro e exibir uma mensagem clara informando que o campo é obrigatório. <br>

**Resultado Obtido:** O sistema bloqueou a continuidade do cadastro e exibiu mensagem solicitando o preenchimento do campo obrigatório.<br>

**Status: PASS** <br><br>

### Evidência
![Campo nome em branco](../Evidências/TC01_REGISTRATION/TC01_REGISTRATION_011_Nome_Ausente.png)

**TC_006.** Deixar o campo "Sobrenome" em branco <br>

**Resultado esperado:** O sistema deve impedir a continuidade do cadastro e exibir uma mensagem clara informando que o campo é obrigatório. <br>

**Resultado Obtido:** O sistema bloqueou a continuidade do cadastro e exibiu mensagem solicitando o preenchimento do campo obrigatório.<br>

**Status: PASS** <br><br>

### Evidência
![Campo sobrenome em branco](../Evidências/TC01_REGISTRATION/TC01_REGISTRATION_010_Sobrenome_Ausente.png)

**TC_007.** Deixar o campo "Senha" em branco <br>

**Resultado esperado:** O sistema deve impedir a continuidade do cadastro e exibir uma mensagem clara informando que o campo é obrigatório. <br>

**Resultado Obtido:**  O sistema bloqueou a continuidade do cadastro e exibiu mensagem solicitando o preenchimento do campo obrigatório.<br>

**Status: PASS** <br><br>

### Evidência
![Campo senha em branco](../Evidências/TC01_REGISTRATION/TC01_REGISTRATION_009_Senha_ausente.png)

Validação de Campos <br><br>


**TC_008.** Inserir números nos campo "Nome" <br>

**Resultado esperado:** O sistema não deve permitir a inserção de números ou símbolos nos campos "Nome" e "Sobrenome" e deve exibir uma mensagem informando que apenas caracteres alfabéticos são permitidos.<br>

**Resultado Obtido:** O sistema permitiu a inserção de números nos campos "Nome" e "Sobrenome" e aprovou a criação do cadastro sem exibir mensagens de validação.<br>

**Status: Fail** <br>

**Bug relacionado:** BUG01_Registro_Nome.md

**Severidade:** Média <br>

**Prioridade:** Média <br><br>

### Evidência <br>

![Sistema aprova criação de cadastro com números no lugar do nome no campo nome](../Evidências/TC01_REGISTRATION/TC01_REGISTRATION_007_Cadastro-de-Usuario-com-Numeros-BUG.png) <br><br>
**Conta Criada com Números no lugar do nome** <br><br>
![Prova da criação do cadastro aprovada pelo sistema](../Evidências/TC01_REGISTRATION/TC01_REGISTRATION_006_Criacao-Aprovada-pelo-Sistema-BUG.png) <br><br>


**TC_009.** Inserir e-mail inválido no campo "E-mail" <br>

**Resultado esperado:** O sistema deve impedir a criação do cadastro e exibir uma mensagem de erro informando que o e-mail inserido é inválido.<br>

**Resultado Obtido:**  O sistema não concluiu o cadastro, porém não exibiu nenhuma mensagem de erro informando o motivo da falha.<br>

**OBS:** Foi observado que, ao inserir um e-mail inválido no campo "E-mail", o sistema não 
apresenta nenhuma mensagem de validação ao usuário. A ausência de feedback pode gerar 
dúvida sobre o motivo pelo qual o cadastro não foi concluído. Recomenda-se a implementação 
de uma mensagem clara informando que é necessário inserir um e-mail válido para prosseguir 
com o cadastro. <br>

**Status: FAIL** <br><br>

### Evidências <br>
![E-mail inválido](../Evidências/TC01_REGISTRATION/TC01_REGISTRATION_013_Ausencia_de_infomacao_fail.png) <br><br>



**TC_010.** Inserir senha com apenas 1 caractere (ex: A ou 1) <br>

**Resultado esperado:** O sistema deve impedir a criação do cadastro e exibir mensagem informando os requisitos mínimos de senha.
<br>

**Resultado Obtido:** O sistema bloqueou a criação do cadastro ao identificar que a senha não atende aos requisitos mínimos e apresentou mensagem "A senha deve ter entre 4 e 20 caracteres!".<br>

**Status: PASS** <br><br>

### Evidência
![Senha com apenas um caractere](../Evidências/TC01_REGISTRATION/TC01_REGISTRATION_008_Senha_Invalida.png)
