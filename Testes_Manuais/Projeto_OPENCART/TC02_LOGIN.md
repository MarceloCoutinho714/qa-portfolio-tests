## Feature: TC_LOGIN_001 - Login

Ambiente: Web/Edge/Windows

Pré-condição: Usuário acessar área de login da Opencart. <br>

Passos:
1. Acessar site da Opencart
2.  Clicar em minha conta e clicar em entrar.
3.  Informar e-mail e senha válidos previamente cadastrados. <br><br><br>
**Regra de Negócio**

O sistema deve permitir o acesso à conta apenas quando o usuário informar credenciais válidas 
(e-mail e senha cadastrados corretamente), bloqueando o login e exibindo mensagem 
apropriada quando as informações forem inválidas ou estiverem incompletas. <br><br>   

Testes Funcionais - Fluxo Principal <br><br>

**TC_001.** Realizar login com credenciais válidas (e-mail e senha cadastrados) <br>

**Resultado Esperado:** Sistema deve autenticar o usuário e permitir acesso à conta. <br>

**Resultado Obtido:** Sistema autenticou o usuário com sucesso e permitiu o acesso. <br>

**Status: PASS** <br><br>

## Evidência <br>

![Login com Sucesso](Evidências/TC02_LOGIN/Sucesso.png) <br><br>

Fluxo Alternativo <br><br>

**TC_002.** Inserir e-mail inválido no campo e-mail <br>

**Resultado Esperado:** Sistema deve exibir mensagem de erro informando que o e-mail ou senha 
são inválidos. <br>

**Resultado Obtido:** Sistema exibiu mensagem "não há correspondência para e-mail ou senha". <br>

**Status: PASS** <br><br>

**TC_003.** Inserir senha inválida no campo senha <br>

**Resultado Esperado:** Sistema deve exibir mensagem de erro informando que o e-mail ou senha 
são inválidos. <br>

**Resultado Obtido:** Sistema exibiu mensagem "não há correspondência para e-mail ou senha". <br>

**Status: PASS** <br><br>

Validação de campos <br><br>

**TC_004.** Tentar realizar login com campo e-mail vazio <br>

**Resultado Esperado:** Sistema não deve autenticar o usuário quando o campo e-mail estiver 
vazio e deve exibir mensagem informando que os dados são inválidos ou obrigatórios. <br>

**Resultado Obtido:**  Sistema não permitiu o login com o campo e-mail vazio e exibiu mensagem 
de erro informando que não há correspondência para e-mail ou senha. <br>

**Status: PASS** <br><br>

**TC_005.** Tentar realizar login com campo senha vazio <br>

**Resultado Esperado:** Sistema não deve autenticar o usuário quando o campo senha estiver 
vazio e deve exibir mensagem informando que os dados são inválidos ou obrigatórios. <br>

**Resultado Obtido:**  Sistema não permitiu o login com o campo senha vazio e exibiu mensagem 
de erro informando que não há correspondência para e-mail ou senha. <br>

**Status: PASS** <br><br>

Teste de Segurança / Regra de Proteção de Conta <br><br>

**TC_006.** Verificar limite de tentativas de login com senha incorreta (proteção contra múltiplas 
tentativas) <br>

**Resultado Esperado:** Após 5 tentativas consecutivas de login com senha incorreta, o sistema 
deve bloquear temporariamente a conta e notificar o usuário por e-mail sobre a atividade 
suspeita. <br>

**Resultado Obtido:** Sistema não limita a quantidade de tentativas de login com senha incorreta, 
permitindo tentativas ilimitadas. <br>

**Status: FAIL** <br><br>

