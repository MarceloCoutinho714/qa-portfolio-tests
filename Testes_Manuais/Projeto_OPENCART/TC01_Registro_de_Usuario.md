## Feature: Cadastro de Usuário

Ambiente: Web/Edge/Windows

Pré-condição: Usuário acessar página inicial da Opencart<br>

Passos:
1. Clicar em minha conta 
2. Clicar em cadastrar
3. Inserir um nome válido no campo "Primeiro Nome"
4. Inserir um sobrenome válido no campo “Sobrenome”
5. Inserir um email válido (ex: marcos_qa@gmail.com)
6. Inserir uma senha válida (mínimo 6 caracteres)
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

**TC_002.** Inserir sobrenome válido no campo "Sobrenome" <br><br>

**Resultado esperado:** O sistema deve aceitar o sobrenome inserido, não exibir mensagens de erro e permitir a continuidade do cadastro.<br>

**Resultado Obtido:** O sistema aceitou o sobrenome inserido sem apresentar mensagens de erro e permitiu a continuidade do cadastro.<br>

**Status: PASS** <br><br>


**TC_003.** Inserir e-mail válido no campo "E-mail" <br>

**Resultado esperado:** O sistema deve aceitar o e-mail inserido no formato válido, não exibir mensagens de erro e permitir a continuidade do cadastro.<br>

**Resultado Obtido:** O sistema aceitou o e-mail inserido sem apresentar mensagens de erro e permitiu a continuidade do cadastro. <br>

**Status: PASS** <br><br>


**TC_004.** Inserir senha com caracteres válidos <br>

**Resultado esperado:** O sistema deve aceitar a senha inserida conforme os critérios mínimos definidos, não exibir mensagens de erro e permitir a conclusão do cadastro. <br>

**Resultado Obtido:** O sistema aceitou a senha inserida sem apresentar mensagens de erro e permitiu a conclusão do cadastro. <br>

**Status: PASS** <br><br>

### Resultado Final do Fluxo <br>
**Resultado esperado:** O sistema deve validar todos os campos obrigatórios, criar a conta com sucesso, redirecionar o usuário para a página "Minha Conta" e exibir a mensagem "Sua conta foi criada!". O usuário deve permanecer autenticado no sistema. <br>

**Resultado obtido:** O sistema validou os campos corretamente, criou a conta com sucesso, redirecionou o usuário para a página "Minha Conta" e exibiu a mensagem de confirmação. O usuário permaneceu logado após o cadastro.<br>

## Evidências <br>

Evidências coletadas durante a execução do teste: <br>

 **Sucesso**
![Cadastro realizado com sucesso](Evidências/TC01_REGISTRATION/Cadastro-com-Sucesso.png) <br><br>


Fluxo Alternativo <br><br>


**TC_005.** Deixar o campo "Nome" em branco <br>

**Resultado esperado:** O sistema deve impedir a continuidade do cadastro e exibir uma mensagem clara informando que o campo é obrigatório. <br>

**Resultado Obtido:** O sistema bloqueou a continuidade do cadastro e exibiu mensagem solicitando o preenchimento do campo obrigatório.<br>

**Status: PASS** <br><br>


**TC_006.** Deixar o campo "Sobrenome" em branco <br>

**Resultado esperado:** O sistema deve impedir a continuidade do cadastro e exibir uma mensagem clara informando que o campo é obrigatório. <br>

**Resultado Obtido:** O sistema bloqueou a continuidade do cadastro e exibiu mensagem solicitando o preenchimento do campo obrigatório.<br>

**Status: PASS** <br><br>


**TC_007.** Deixar o campo "Senha" em branco <br>

**Resultado esperado:** O sistema deve impedir a continuidade do cadastro e exibir uma mensagem clara informando que o campo é obrigatório. <br>

**Resultado Obtido:**  O sistema bloqueou a continuidade do cadastro e exibiu mensagem solicitando o preenchimento do campo obrigatório.<br>

**Status: PASS** <br><br>


Validação de Campos <br><br>


**TC_008.** Inserir números nos campo "Nome" <br>

**Resultado esperado:** O sistema não deve permitir a inserção de números ou símbolos nos campos "Nome" e "Sobrenome" e deve exibir uma mensagem informando que apenas caracteres alfabéticos são permitidos.<br>

**Resultado Obtido:** O sistema permitiu a inserção de números nos campos "Nome" e "Sobrenome" e aprovou a criação do cadastro sem exibir mensagens de validação.<br>

**Status: BUG** <br>

**Severidade:** Média <br>

**Prioridade:** Média <br><br>

## Evidência <br>

**BUG** <br><br>
**Cadastro com Númeors** <br>
![Sistema aprova criação de cadastro com números no lugar do nome no campo nome](Evidências/TC01_REGISTRATION/Cadastro-de-Usuario-com-Numeros-BUG.png) <br><br>
**Conta Criada com Números no lugar do nome** <br><br>
![Prova da criação do cadastro aprovada pelo sistema](Evidências/TC01_REGISTRATION/Criacao-Aprovada-pelo-Sistema-BUG.png) <br><br>


**TC_009.** Inserir e-mail inválido no campo "E-mail" <br>

**Resultado esperado:** O sistema deve impedir a criação do cadastro e exibir uma mensagem de erro informando que o e-mail inserido é inválido.<br>

**Resultado Obtido:**  O sistema não concluiu o cadastro, porém não exibiu nenhuma mensagem de erro informando o motivo da falha.<br>

**OBS:** Foi observado que, ao inserir um e-mail inválido no campo "E-mail", o sistema não 
apresenta nenhuma mensagem de validação ao usuário. A ausência de feedback pode gerar 
dúvida sobre o motivo pelo qual o cadastro não foi concluído. Recomenda-se a implementação 
de uma mensagem clara informando que é necessário inserir um e-mail válido para prosseguir 
com o cadastro. <br>

**Status: FAIL** <br><br>

## Evidências <br>

**Erro** 
![Ausência de mensgem de erro por e-mail inválido](Evidências/TC01_REGISTRATION/Ausencia-de-Informacao-Erro.png) <br><br>



**TC_010.** Inserir senha com apenas 1 caractere (ex: A ou 1) <br>

**Resultado esperado:** O sistema deve impedir a criação do cadastro e exibir mensagem informando os requisitos mínimos de senha.
<br>

**Resultado Obtido:** O sistema bloqueou a criação do cadastro ao identificar que a senha não atende aos requisitos mínimos.<br>

**Status: PASS** <br><br>

