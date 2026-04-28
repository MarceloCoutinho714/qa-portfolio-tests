## Feature: Pesquisa por produtos

Ambiente: Web/Edge/Windows

Pré-condição:  Usuário acessar página inicial da Opencart. <br>

**Test Data**<br>

Pesquisa válida: Iphone<br>
Pesquisa inexistente: XYZ123<br>
Pesquisa com caracteres especiais: @#$%<br>
Pesquisa com espaços: "   "<br>
Pesquisa com variação: iphone / IPHONE<br>


Passos:
1. Clicar no campo de pesquisa 
2. Digitar título específico conforme Test Data
3. Clicar em pesquisar <br><br><br>

**Regra de Negócio**

O sistema deve retornar produtos cujo nome ou descrição esteja relacionado ao termo digitado 
pelo usuário no campo de pesquisa. <br><br>   

Testes Funcionais - Fluxo Principal <br><br>

**TC_001.** Buscar produto pelo nome específico <br>

**Resultado Esperado:** O sistema deve exibir uma lista de produtos cujo nome ou descrição contenha o termo "Iphone", apresentando informações como nome, preço e imagem do produto.<br>

**Resultado Obtido:** O sistema exibiu produtos relacionados ao termo pesquisado "iPhone" com imagem, descrição e preço. <br>

**Status: PASS** <br><br>

Fluxo Alternativo <br><br>

**TC_002.** Realizar busca com campo vazio <br>

**Resultado Esperado:** O sistema não deve retornar resultados ou deve informar que é 
necessário inserir um termo para realizar a busca. <br>

**Resultado Obtido:** O sistema não retornou resultados. <br>

**Status: PASS** <br><br>

**TC_003.** Buscar produto com cor específica <br>

**Resultado Esperado:** O sistema deve retornar produtos correspondentes ao termo pesquisado, 
incluindo a cor especificada. <br>

**Resultado Obtido:** O sistema retornou o produto com a cor informada. <br>

**Status: PASS** <br><br>

**TC_004.** Buscar produto com memória específica <br>

**Resultado Esperado:** O sistema deve retornar produtos que correspondam à memória 
especificada na busca. <br>

**Resultado Obtido:**  N/A <br>

**Status: Não Aplicável** <br><br>

**TC_005.** Aplicar filtros e categorias nos resultados <br>

**Resultado Esperado:** O sistema deve ordenar ou filtrar os resultados conforme a opção 
selecionada pelo usuário. <br>

**Resultado Obtido:**  N/A <br>

**Status: Não Aplicável** <br><br>

**TC_006.** Inserir caracteres aleatórios no campo de busca <br>

**Resultado Esperado:**  O sistema não deve retornar resultados para termos que não 
correspondam a produtos cadastrados. <br>

**Resultado Obtido:** O sistema não retornou resultados. <br>

**Status: PASS** <br><br>
