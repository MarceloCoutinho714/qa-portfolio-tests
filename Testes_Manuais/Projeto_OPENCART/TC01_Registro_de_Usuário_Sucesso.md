## Feature: TC01 - Verificar se o usuário consegue se registrar com sucesso usando dados válidos

Ambiente: Web/Edge/Windows

Pré-condição: Usuário acessar página inicial da Opencart
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
**Resultado esperado:** Sistema redireciona para página "Minha Conta" e exibe mensagem "Sua conta foi criada!" <br>

**Resultado Obtido:** Sistema aprovou o cadastro redirecionando usuário a página "Minha Conta" <br>

**Status: PASS** <br><br>

**TC_002.** Inserir sobrenome válido no campo "Sobrenome" <br><br>

**Resultado esperado:** Sistema aceita o sobrenome e permite continuar o cadastro. <br>

**Resultado Obtido:** Sistema aprovou o cadastro.<br>

**Status: PASS** <br><br>


**TC_003.** Inserir e-mail válido no campo "E-mail" <br>

**Resultado esperado:** Sistema aceita e-mail válido e permite continuar o cadastro. <br>

**Resultado Obtido:** Sistema aprovou o cadastro. <br>

**Status: PASS** <br><br>


**TC_004.** Inserir senha com caracteres válidos <br>

**Resultado esperado:** Sistema aceita senha válida e conclui o cadastro. <br>

**Resultado Obtido:** Sistema aprovou o cadastro. <br>

**Status: PASS** <br><br>

## Evidências <br>

Evidências coletadas durante a execução do teste: <br>

 **Sucesso**
![Cadastro realizado com sucesso](Evidências/TC01_REGISTRATION/Cadastro-com-Sucesso.png) <br><br>


Fluxo Alternativo <br><br>


**TC_005.** Deixar o campo "Nome" em branco <br>

**Resultado esperado:** Sistema deve exibir mensagem informando que o campo é obrigatório. <br>

**Resultado Obtido:** Sistema exibiu mensagem solicitando preenchimento do campo 
obrigatório. <br>

**Status: PASS** <br><br>


**TC_006.** Deixar o campo "Sobrenome" em branco <br>

**Resultado esperado:** Sistema deve exibir mensagem informando que o campo é obrigatório. <br>

**Resultado Obtido:**  Sistema exibiu mensagem solicitando preenchimento do campo 
obrigatório. <br>

**Status: PASS** <br><br>


**TC_007.** Deixar o campo "Senha" em branco <br>

**Resultado esperado:** Sistema deve exibir mensagem informando que o campo é obrigatório. <br>

**Resultado Obtido:**  Sistema exibiu mensagem solicitando preenchimento do campo 
obrigatório. <br>

**Status: PASS** <br><br>


Validação de Campos <br><br>


**TC_008.** Inserir números e símbolos nos campos "Nome" e "Sobrenome" <br>

**Resultado esperado:** Sistema deve exibir mensagem informando que apenas letras são 
permitidas. <br>

**Resultado Obtido:**  Sistema permitiu a criação de cadastro utilizando números e símbolos. <br>

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

**Resultado esperado:** O sistema deve exibir uma mensagem de erro informando que o e-mail 
inserido é inválido e solicitar a inserção de um e-mail válido. <br>

**Resultado Obtido:**  Sistema não exibiu mensagem de erro e não concluiu o cadastro. <br>

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

**Resultado esperado:** Sistema não deve permitir a criação do cadastro e deve exibir mensagem informando requisitos mínimos de senha. <br>

**Resultado Obtido:** Sistema não aprovou a criação do cadastro sem os requisitos mínimos. <br>

**Status: PASS** <br><br>

