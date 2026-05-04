## Feature: Pesquisa por produtos

Ambiente: Web/Edge/Windows

Pré-condição:  Usuário acessar página inicial da Opencart. <br>

**Test Data**<br>

Pesquisa válida: Iphone<br>
Pesquisa inexistente: XYZ123<br>
Pesquisa com caracteres especiais: @#$% <br>
Pesquisa com espaços: "   "<br>
Pesquisa com variação: iphone / IPHONE<br>


Passos:
1. Clicar no campo de pesquisa 
2. Digitar termo conforme Test Data
3. Clicar em "pesquisar" <br><br>

**Regra de Negócio**

O sistema deve retornar produtos cujo nome ou descrição esteja relacionado ao termo digitado 
pelo usuário no campo de pesquisa. <br><br>   

Testes Funcionais - Fluxo Principal <br><br>

**TC_001.** Buscar produto pelo nome específico <br>

**Resultado Esperado:** O sistema deve exibir uma lista de produtos cujo nome ou descrição contenha o termo "Iphone", apresentando informações como nome, preço e imagem. <br>

**Resultado Obtido:** O sistema exibiu produtos relacionados ao termo "Iphone", incluindo nome, preço e imagem.<br>

**Status: PASS** <br><br>

### Evidência 

![Busca de produto especifico feita com secesso!](../Evidências/TC03_SEARCH/positivo/TC03_SEARCH_001_Busca_sucesso.png) <br><br>


Fluxo Alternativo <br><br>

**TC_002.** Realizar busca com campo vazio 

**Resultado Esperado:** O sistema não deve retornar resultados e pode exibir mensagem informando que nenhum termo foi inserido.<br>

**Resultado Obtido:** O sistema não retornou resultados para o campo vazio e apresentou mensagem "Não existe nenhum produto que atenda aos critérios de busca." <br>

**Status: PASS** <br><br>

### Evidência
![Busca com campos vazios.](../Evidências/TC03_SEARCH/negativo/TC03_SEARCH_002_Busca_Campo_Vazio.png) <br><br>

**TC_003.** Busca por termo inexistente (ex: XYZ123 )

**Resultado Esperado:** O sistema deve exibir mensagem informando que nenhum produto foi encontrado.<br>

**Resultado Obtido:** O sistema não retornou resultados para o termo pesquisado e apresentou mensagem "Não existe nenhum produto que atenda aos critérios de busca."<br>

**Status: PASS** <br><br>

### Evidência
![Busca com termo inexistente.](../Evidências/TC03_SEARCH/negativo/TC03_SEARCH_003_Busca_Termo_Inexistente.png) <br><br>

**TC_004.** Busca por caracteres especiais 

**Resultado Esperado:** O sistema não deve retornar resultados para caracteres inválidos e pode exibir mensagem informativa. <br>

**Resultado Obtido:** O sistema não retornou resultados para caracteres especiais e apresentou mensagem "Não existe nenhum produto que atenda aos critérios de busca." <br>

**Status: PASS** <br><br>

### Evidência
![Busca com caracteres especiais.](../Evidências/TC03_SEARCH/negativo/TC03_SEARCH_004_Busca_Caracteres_Especiais.png) <br><br>

**TC_005.** Diferenciação entre Maiúsculas e minúsculas

**Resultado Esperado:** O sistema deve retornar os mesmos resultados independentemente do uso de letras maiúsculas ou minúsculas.<br>

**Resultado Obtido:** O sistema retornou os mesmos resultados para "iphone" e "IPHONE". <br>

**Status: PASS** <br><br>

### Evidência
**Maiúsculas**<br><br>

![Digitar todo o termo em maiúsculo.](../Evidências/TC03_SEARCH/positivo/TC03_SEARCH_005_Busca_Diferenciacao_Maiuscula.png) <br><br><br>

### Evidência
**Minúsculas**<br><br>

![Digitar todo o termo em minúsculo.](../Evidências/TC03_SEARCH/positivo/TC03_SEARCH_006_Busca_Diferenciacao_Minuscula.png) <br><br>

**TC_006.** Espaços extras 

**Resultado Esperado:** O sistema deve ignorar espaços extras antes ou depois do termo e retornar resultados normalmente. <br>

**Resultado Obtido:** O sistema retornou resultados corretamente mesmo com espaços extras no termo. <br>

**Status: PASS** <br><br>




