## Feature: Gerenciamento de Carrinho de Compras 

Ambiente: Web/Edge/Windows

Pré-condição: Usuário acessar página inicial da Opencart. <br>

**Test Data**

Produto: iPhone <br>
Quantidade Inicial: 1 <br>
Quantidade Alterada: 3 <br>

Passos:
1. Acessar o site Opencart
2. Selecionar um produto
3. Clicar em "Adicionar ao carrinho"
4. Acessar "Meu Carrinho" <br><br><br>
**Regra de Negócio**

O sistema deve permitir que o usuário adicione produtos ao carrinho, visualize os itens 
selecionados e atualize ou remova produtos, garantindo que apenas itens válidos e disponíveis 
sejam mantidos no carrinho antes da finalização da compra. <br><br>   

Testes Funcionais - Fluxo Principal <br><br>

**TC_001.**  Adicionar produto ao carrinho <br><br>
**Resultado Esperado:** O sistema deve adicionar o produto ao carrinho, atualizar o contador de itens e exibir mensagem de sucesso confirmando a ação. <br>

**Resultado Obtido:** O sistema adicionou o produto ao carrinho, atualizou o contador e exibiu a mensagem: "Sucesso: Você adicionou o iPhone ao seu carrinho de compras!". <br>

**Status: PASS** <br><br>

### Evidência
**Mensagem de Produto Adicionado** <br><br>

![Produto adicionado ao carrinho com sucesso.](../Evidências/TC04_CART/Sucesso/TC04_CART_001_Adicionado_Mensagem_Sucesso.png)<br><br>


**TC_002.** Visualizar produto no carrinho <br><br>

**Resultado Esperado:** O sistema deve exibir o produto adicionado no carrinho, apresentando informações como nome, preço e quantidade, além de permitir alteração ou remoção. <br>

**Resultado Obtido:** O produto foi exibido corretamente no carrinho, com opções de alterar quantidade e remover.<br>

**Status: PASS** <br><br>

### Evidência
**Confirmação de produto adicionado**<br><br>

![Produto aparecce no carrinho com sucesso](../Evidências/TC04_CART/Sucesso/TC04_CART_002_Adicionado_Sucesso.png)<br><br>


**TC_003.**  Prosseguir para checkout <br>

**Resultado Esperado:** O sistema deve redirecionar o usuário para a página de checkout, solicitando dados de endereço e pagamento.<br>

**Resultado Obtido:** N/A – Funcionalidade de checkout indisponível no ambiente de teste <br>

**Status: BLOCKED** <br>

**Motivo:** Funcionalidade não disponível no ambiente. <br><br>


**TC_004.** Remover produto do carrinho <br>

**Resultado Esperado:** O sistema deve remover o produto selecionado do carrinho e exibir mensagem de confirmação. <br>

**Resultado Obtido:** O sistema removeu o produto com sucesso e exibiu a mensagem: "Sucesso: Você removeu um item do seu carrinho de compras!". <br>

**Status: PASS** <br><br>

### Evidência

![Produto removido do carrinho com sucesso.](../Evidências/TC04_CART/Sucesso/TC04_CART_003_Removido_Sucesso.png)<br><br>




**TC_005.** Alterar quantidade de produto no carrinho <br>

**Resultado Esperado:** O sistema deve permitir alterar a quantidade do produto e atualizar o carrinho, recalculando valores e exibindo mensagem de confirmação. <br>

**Resultado Obtido:** O sistema atualizou a quantidade corretamente e exibiu a mensagem: "Sucesso: Você modificou seu carrinho de compras!". <br>

**Status: PASS** <br><br>

### Evidência

![Quantidade alterada com sucesso.](../Evidências/TC04_CART/Sucesso/TC04_CART_004_Alterado_Sucesso.png)<br><br>


**TC_006.** Carrinho vazio após remoção de item <br>

**Resultado Esperado:** Ao remover todos os itens, o sistema deve exibir mensagem indicando que o carrinho está vazio. <br>

**Resultado Obtido:** O carrinho ficou vazio e exibiu a mensagem: "Seu carrinho de compras está vazio!". <br>

**Status: PASS** <br><br>

### Evidência

![Carrinho vazio com sucesso](../Evidências/TC04_CART/Sucesso/TC04_CART_005_Carrinho_vazio_Sucesso.png)<br><br>


**TC_007.** Remover um produto quando há múltiplos itens no carrinho <br>

**Resultado Esperado:** O sistema deve remover apenas o item selecionado e manter os demais produtos no carrinho, atualizando o contador e preços.<br>

**Resultado Obtido:** O sistema removeu corretamente o item selecionado, manteve os demais produtos no carrinho atualizando o contador e preços com sucesso. <br>

**Status: PASS** <br><br>

### Evidência 
**Antes** <br>
![Itens adicionados](../Evidências/TC04_CART/Sucesso/TC04_CART_009_Produtos_Atualizados_Sucesso.png)<br><br>

**Depois** <br>
![Carrinho atualizado com sucesso após item ter sido removido](../Evidências/TC04_CART/Sucesso/TC04_CART_012_Um_Produto_Removido_Sucesso.png)<br><br>


**TC_008.** Adicionar múltiplos produtos ao carrinho <br>

**Resultado Esperado:** O sistema deve permitir adicionar diferentes produtos ao carrinho simultaneamente. <br>

**Resultado Obtido:** O sistema permitiu adicionar múltiplos produtos distintos ao carrinho com sucesso. <br>

**Status: PASS** <br><br>

### Evidência

![Múltiplos produtos adicionados com sucesso](../Evidências/TC04_CART/Sucesso/TC04_CART_006_Multiplos_Produtos_Adicionados_Sucesso.png)<br><br>

Fluxos Alternativo - Validação de Carrinho <br><br>


**TC_009.** Atualização de preço, peso e quantidade ao adicionar ou remover produtos <br>

**Resultado Esperado:** O sistema deve atualizar automaticamente o valor total, a quantidade de itens e o peso total do carrinho sempre que um produto for adicionado, removido ou tiver sua quantidade alterada. <br>

**Resultado Obtido:** O sistema atualiza corretamente o valor total e a quantidade de itens. No entanto, foi identificado que, para **alguns produtos**, o peso total do carrinho não é atualizado após alterações. <br>

O comportamento não ocorre de forma consistente para todos os itens, indicando possível falha associada a produtos específicos ou regras de cálculo.

Essa inconsistência pode impactar diretamente o cálculo de frete, emissão de nota fiscal e processos logísticos, especialmente em cenários onde o peso influencia restrições de transporte (ex: transporte aéreo).<br>

**Status: Fail** <br>

**Observação:** <br>

Recomenda-se identificar quais produtos apresentam o problema e validar possíveis diferenças em atributos como peso cadastrado, tipo de produto ou regras específicas aplicadas. <br>

**Bug relacionado:** BUG02_Peso_de_Itens_do_Carrinho_Não_Atualiza

**Severidade:** <br>
Alta <br>

**Prioridade:** <br>
Alta <br><br>

### Evidência
**Antes**<br>
![Preço atual da soma dos produtos](../Evidências/TC04_CART/)<br><br>

**Depois**
![Preço atualizado conforme um produto é adicionado ou removido, peso apresenta inconsistência](../Evidências/TC04_CART/)<br><br>


**TC_010.** Verificar persistência do carrinho após atualizar ou reabrir a página <br>

**Resultado Esperado:** O sistema deve manter os produtos no carrinho após atualização da página ou reabertura do site durante a mesma sessão.<br>

**Resultado Obtido:** Os produtos permaneceram no carrinho após atualização e reabertura do site. <br>

**Status: PASS** <br><br>

## Evidência <br>
![Carrinho apresenta persistência com sucesso](../Evidências/TC04_CART/Sucesso/TC04_CART_008_Persistencia_do_Carrinho_Sucesso.png) <br><br>

