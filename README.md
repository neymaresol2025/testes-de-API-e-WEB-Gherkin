# testes-de-API-e-WEB-Gherkin
Gherkin
----------
Feature : Busca de Produto  
Scenario : Usuário realiza a busca de um produto pelo nome  
Given que o usuário acessa o site Advantage Online Shopping  
When  ele digita o nome do produto no campo de busca  
And clica no botão de pesquisar  
Then o sistema exibe os produtos correspondentes à busca  
And o produto pesquisado aparece na lista de resultados
Feature Adicionar Produto ao Carrinho  
 
 Scenario : Usuário adiciona um produto ao carrinho  
  Given que o usuário está na página de detalhes de um produto  
  When ele seleciona a quantidade desejada  
  And clica no botão "Adicionar ao Carrinho"  
  Then o sistema adiciona o produto ao carrinho  
  And exibe uma notificação confirmando a adição
Feature Validação do Carrinho na Tela de Pagamento  

Scenario: Usuário verifica os produtos antes do pagamento  
  Given que o usuário tem produtos adicionados ao carrinho  
  When ele acessa a página do carrinho de compras  
  Then o sistema exibe os produtos corretos com nome, quantidade e preço  
  When o usuário avança para a tela de pagamento  
  Then os mesmos produtos são exibidos corretamente para finalizar a compra
Feature: Remover Produto do Carrinho  

 Scenario : Usuário remove um produto do carrinho  
  Given que o usuário tem um produto no carrinho  
  When ele clica no botão de remover ao lado do produto  
  Then o sistema remove o produto do carrinho  
  And exibe uma mensagem confirmando a remoção
Feature: Restrição de Finalização de Compra  

 Scenario : Usuário tenta finalizar a compra com o carrinho vazio  
  Given que o usuário acessa o carrinho de compras  
  And o carrinho está vazio  
  When ele tenta clicar no botão "Finalizar Compra"  
  Then o sistema não permite a ação  
  And exibe uma mensagem informando que é necessário adicionar produtos antes de prosseguir
