ID do Bug: BUG02_Peso_Carrinho_Não_Atualiza

Título: Carrinho não atualiza o peso total ao adicionar ou remover produtos <br><br>

Tipo: Bug Funcional <br>
Ferramenta usada: Teste Manual (Navegador) <br>
Módulo: Carrinho de Compras <br>
Tipo de teste: Teste Funcional Manual <br><br>

Ambiente

Ambiente: Aplicação web de testes <br>
Ferramenta: Navegador (Microsoft Edge) <br>
Data do teste: 29/04/2026 <br><br>

Pré-condição

Usuário deve estar com acesso ao sistema e com produtos disponíveis para adicionar ao carrinho. <br><br>

Passos para Reproduzir
Acessar o sistema. <br>
Adicionar um produto ao carrinho. <br>
Verificar o peso total exibido no carrinho. <br>
Adicionar ou remover outros produtos. <br>
Alterar a quantidade de um produto já adicionado. <br>
Observar a atualização do peso total do carrinho. <br><br>
Resultado Esperado

O sistema deve atualizar automaticamente o valor total, a quantidade de itens e o peso total do carrinho sempre que um produto for adicionado, removido ou tiver sua quantidade alterada. <br><br>

Resultado Obtido

O sistema atualiza corretamente o valor total e a quantidade de itens. No entanto, foi identificado que o peso total do carrinho não é atualizado após alterações nos produtos.

Em alguns casos, o comportamento ocorre apenas com determinados itens, indicando possível inconsistência nos dados ou ausência de validação adequada pelo sistema. <br><br>

Impacto

A inconsistência no cálculo do peso total pode impactar diretamente:

Cálculo de frete
Emissão de nota fiscal
Processos logísticos

Esse problema é especialmente crítico em cenários onde o peso influencia regras de transporte, como no transporte aéreo. <br><br>

Severidade

Alta <br><br>

Prioridade

Alta <br><br>
