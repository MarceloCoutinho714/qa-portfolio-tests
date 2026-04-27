## Feature: TC_CART_001 - Gerenciamento de Carrinho de Compras 

Ambiente: Web/Edge/Windows

Pré-condição: Usuário acessar página inicial da Opencart. <br>

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
**Resultado Esperado:** : Ao clicar em "Adicionar ao carrinho", o sistema deve incluir o produto no 
carrinho do usuário. <br>

**Resultado Obtido:** Sistema adicionou o produto ao carrinho com sucesso. <br>

**Status: PASS** <br><br>

**TC_002.** Visualizar produto no carrinho <br><br>

**Resultado Esperado:** Ao acessar o carrinho, o sistema deve exibir o produto previamente 
adicionado. <br>

**Resultado Obtido:** Produto exibido corretamente no carrinho. <br>

**Status: PASS** <br><br>


**TC_003.**  Prosseguir para checkout <br>

**Resultado Esperado:** Ao clicar em "Confirmar compra" ou "Checkout", o sistema deve 
redirecionar o usuário para a página de finalização da compra. <br>

**Resultado Obtido:** N/A - O site de teste não permite prosseguir para o checkout. <br>

**Status: BLOCKED** <br><br>


**TC_004.** Remover produto do carrinho <br>

**Resultado Esperado:** O sistema deve remover o produto selecionado do carrinho. <br>

**Resultado Obtido:**  Produto removido com sucesso do carrinho. <br>

**Status: PASS** <br><br>


**TC_005.** Alterar quantidade de produto no carrinho <br>

**Resultado Esperado:**  O sistema deve permitir alterar a quantidade do produto e atualizar o 
carrinho corretamente. <br>

**Resultado Obtido:**  Sistema permitiu a alteração da quantidade com sucesso. <br>

**Status: PASS** <br><br>


**TC_006.** Carrinho vazio após remoção de item <br>

**Resultado Esperado:** Quando houver um único produto no carrinho e o mesmo for removido o carrinho deve ficar vazio. <br>

**Resultado Obtido:** Carrinho ficou vazio após a remoção do produto. <br>

**Status: PASS** <br><br>


**TC_007.** Remover um produto quando há múltiplos itens no carrinho <br>

**Resultado Esperado:**  Ao remover um dos produtos, o sistema deve atualizar o carrinho 
exibindo apenas os itens restantes. <br>

**Resultado Obtido:**  Sistema removeu corretamente o produto selecionado e atualizou os itens 
restantes no carrinho. <br>

**Status: PASS** <br><br>


**TC_008.** Adicionar múltiplos produtos ao carrinho <br>

**Resultado Esperado:** O sistema deve permitir adicionar mais de um produto diferente ao 
carrinho. <br>

**Resultado Obtido:** O sistema permitiu adicionar mais produtos distintos ao carrinho com 
sucesso. <br>

**Status: PASS** <br><br>

Fluxos Alternativo <br><br>

Validação do Carrinho <br><br>

**TC_009.** Atualização de preço ao adicionar ou remover produtos <br>

**Resultado Esperado:** O valor total do carrinho deve ser atualizado automaticamente ao 
adicionar ou remover produtos. <br>

**Resultado Obtido:** O sistema atualizou corretamente o valor total após alterações no carrinho. <br>

**Status: PASS** <br><br>


**TC_010.** Verificar persistência do carrinho após atualizar ou reabrir a página <br>

**Resultado Esperado:** : O sistema deve manter os produtos previamente adicionados ao carrinho 
mesmo após o usuário atualizar a página ou fechar e abrir o site novamente dentro da mesma 
sessão. <br>

**Resultado Obtido:**  Após atualizar a página e também após fechar e abrir novamente o site, os 
produtos permaneceram no carrinho corretamente. <br>

**Status: PASS** <br><br>

## Evidência <br>
![Carrinho funcionando com sucesso](Evidências/TC01_REGISTRATION/TC04_CART/Prodruto-Adicionado-com-Sucesso.png) <br><br>
