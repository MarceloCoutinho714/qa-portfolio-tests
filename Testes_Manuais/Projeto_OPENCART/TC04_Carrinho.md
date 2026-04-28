## Feature: Gerenciamento de Carrinho de Compras 

Ambiente: Web/Edge/Windows

Pré-condição: Usuário acessar página inicial da Opencart. <br>

**Test Data**
Produto: iPhone
Quantidade Inicial: 1
Quantidade Alterada: 3

Passos:
1. Acessar site Opencart. 
2. Clicar em adicionar ao meu carrinho em um produto específico 
3. Clicar em **Meu Carrinho** <br><br><br>
**Regra de Negócio**

O sistema deve permitir que o usuário adicione produtos ao carrinho, visualize os itens 
selecionados e atualize ou remova produtos, garantindo que apenas itens válidos e disponíveis 
sejam mantidos no carrinho antes da finalização da compra. <br><br>   

Testes Funcionais - Fluxo Principal <br><br>

**TC_001.**  Adicionar produto ao carrinho <br><br>
**Resultado Esperado:** O sistema deve incluir o produto no carrinho, atualizar o ícone/contador do carrinho e exibir mensagem de sucesso confirmando a adição do item. <br>

**Resultado Obtido:** Sistema adicionou o produto ao carrinho com sucesso e apresentou mensagem "Sucesso: Você adicionou o iPhone ao seu carrinho de compras!". <br>

### Evidência
**Mensagem de Adicionado** <br><br>

![Produto adicionado ao carrinho com sucesso.]()<br><br>

**Status: PASS** <br><br>

**TC_002.** Visualizar produto no carrinho <br><br>

**Resultado Esperado:** Ao acessar o carrinho, o sistema deve exibir o produto previamente adicionado no carrinho dando opções de alterar a quantidade e excluir. <br>

**Resultado Obtido:** Produto exibido corretamente no carrinho dando opções ao usuário de alterar quantidade e excluir. <br>

**Status: PASS** <br><br>

### Evidência
**Confirmação de produto adicionado**<br><br>

![Produto adicionado ao carrinho com sucesso.]()<br><br>


**TC_003.**  Prosseguir para checkout <br>

**Resultado Esperado:** Ao clicar em "Confirmar compra" ou "Checkout", o sistema deve 
redirecionar o usuário para a página de finalização da compra e solicitar dados de endereço e pagamento. <br>

**Resultado Obtido:** N/A - O site de teste não permite prosseguir para o checkout. <br>

**Motivo:** Funcionalidade de checkout indisponível no ambiente de teste.

**Status: BLOCKED** <br><br>


**TC_004.** Remover produto do carrinho <br>

**Resultado Esperado:** O sistema deve remover o produto selecionado do carrinho e apresentar mensagem "Produto removido com sucesso". <br>

**Resultado Obtido:** Sistema remove produto com sucesso e apresenta mensagem "Sucesso: Você removeu um item do seu carrinho de compras!" <br>

### Evidência

![Produto removido do carrinho com sucesso.]()<br><br>

**Status: PASS** <br><br>


**TC_005.** Alterar quantidade de produto no carrinho <br>

**Resultado Esperado:**  O sistema deve permitir alterar a quantidade do produto e atualizar o carrinho corretamente informando mensagem "Produto alterado com sucesso" <br>

**Resultado Obtido:**  Sistema permitiu a alteração da quantidade com sucesso e apresentou mensagem "Sucesso: Você modificou seu carrinho de compras!" <br>

**Status: PASS** <br><br>

### Evidência

![Produto removido do carrinho com sucesso.]()<br><br>


**TC_006.** Carrinho vazio após remoção de item <br>

**Resultado Esperado:** Quando todos os itens do carrinho forem excluidos o carrinho deve ficar vazio e exibir mensagem "Carrinho de compras vazio". <br>

**Resultado Obtido:** Carrinho ficou vazio após a remoção do produto e apresentou mensagem "Seu carrinho de compras está vazio!" <br>

**Status: PASS** <br><br>

### Evidência

![Produto removido do carrinho com sucesso.]()<br><br>


**TC_007.** Remover um produto quando há múltiplos itens no carrinho <br>

**Resultado Esperado:**  Ao remover um dos produtos, o sistema deve atualizar o carrinho 
exibindo apenas os itens restantes e exibir mensagem "Item removido do carrinho com sucesso".<br>

**Resultado Obtido:**  Sistema removeu corretamente o produto selecionado e atualizou os itens restantes apresentando mensagem "Sucesso: Você removeu um item do seu carrinho de compras!" <br>

**Status: PASS** <br><br>

### Evidência

![Produto removido do carrinho com sucesso.]()<br><br>


**TC_008.** Adicionar múltiplos produtos ao carrinho <br>

**Resultado Esperado:** O sistema deve permitir adicionar mais de um produto diferente ao 
carrinho. <br>

**Resultado Obtido:** O sistema permitiu adicionar múltiplos produtos distintos ao carrinho com sucesso. <br>

**Status: PASS** <br><br>

### Evidência

![Produto removido do carrinho com sucesso.]()<br><br>

Fluxos Alternativo <br><br>

Validação do Carrinho <br><br>

**TC_009.** Atualização de preço ao adicionar ou remover produtos <br>

**Resultado Esperado:** O valor total do carrinho deve ser atualizado automaticamente ao 
adicionar ou remover produtos. <br>

**Resultado Obtido:** O sistema atualizou corretamente o valor total após alterações no carrinho. <br>

**Status: PASS** <br><br>

### Evidência

![Produto removido do carrinho com sucesso.]()<br><br>


**TC_010.** Verificar persistência do carrinho após atualizar ou reabrir a página <br>

**Resultado Esperado:** : O sistema deve manter os produtos previamente adicionados ao carrinho mesmo após o usuário atualizar a página ou fechar e abrir o site novamente dentro da mesma sessão. <br>

**Resultado Obtido:** Após atualizar a página e também após fechar e abrir novamente o site, os produtos permaneceram no carrinho corretamente. <br>

**Status: PASS** <br><br>

## Evidência <br>
![Carrinho funcionando com sucesso]() <br><br>

