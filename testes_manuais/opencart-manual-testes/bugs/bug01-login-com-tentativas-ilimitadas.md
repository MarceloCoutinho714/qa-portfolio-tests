**Origem:** TC02 - Login_de_Usuário.md

### Bug ID: BUG01_Login_Tentativas_Ilimitadas

Título: Sistema permite tentativas ilimitadas de login com senha incorreta. <br>
Tipo: BUG <br>
Categoria: Segurança / Funcional <br>
Ambiente:  Web / Navegador Edge / Windows <br>
Tipo de teste: Teste Manual / Funcional <br><br>

**Ambiente**

Ambiente: Sistema público de E-commerce <br>
Data do teste: 28/04/2026 <br><br>

**Pré-condição** <br>

Usuário possuir conta previamente cadastrada e acessar a página de login.<br><br>

**Passos para Reproduzir**

1. Acessar a página de login<br>
2. Inserir e-mail válido previamente cadastrado <br>
3. Inserir senha incorreta<br>
4. Clicar em “Entrar“<br>
5. Repetir o processo de 2 à 5 vezes consecutivas<br>

**Resultado Esperado**

O sistema deve limitar o número de tentativas consecutivas de login inválidas (ex: 5 tentativas), bloqueando temporariamente o acesso ou exigindo verificação adicional.

**Resultado Obtido**

O sistema permite tentativas ilimitadas de login com senha incorreta, sem qualquer bloqueio ou mecanismo de proteção.

**Observação**

Durante a execução do teste, foram realizadas múltiplas tentativas consecutivas de login com senha incorreta, sem que o sistema aplicasse qualquer tipo de bloqueio ou limitação.


**Impacto**

A ausência de limitação de tentativas de login pode expor o sistema a ataques de força bruta, aumentando o risco de comprometimento de contas de usuários.

**Severidade**<br>
Alta

**Prioridade**<br>
Alta

**Evidências**<br>

Tentativa_1<br>

![Múltiplas tentativas de loguin com senha inválida](../evidencias/tc02_login/negativo/tc02-login-tentativa-1.png)<br>
Tentativa_2<br>

![Múltiplas tentativas de loguin com senha inválida](../evidencias/tc02_login/negativo/tc02-login-tentativa-2.png)<br>
Tentativa_3<br>

![Múltiplas tentativas de loguin com senha inválida](../evidencias/tc02_login/negativo/tc02-login-tentativa-3.png)<br>
Tentativa_4<br>

![Múltiplas tentativas de loguin com senha inválida](../evidencias/tc02_login/negativo/tc02-login-tentativa-4.png)<br>
Tentativa_5<br>

![Múltiplas tentativas de loguin com senha inválida](../evidencias/tc02_login/negativo/tc02-login-tentativa-5.png)<br>
Tentativa_6<br>

![Múltiplas tentativas de loguin com senha inválida](../evidencias/tc02_login/negativo/tc02-login-tentativa-6.png)<br>


