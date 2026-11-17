# Projeto Blazor - Aula 3

Por que o FormProduto não adiciona o produto direto na lista?
O `FormProduto` não adiciona o produto diretamente na lista para manter o princípio de responsabilidade única e isolamento do componente filho, permitindo que ele seja reaproveitado em outros contextos (como no futuro cadastro de categorias).
Quem faz a adição é a página pai (`Produtos.razor`), que gerencia o estado da lista. O filho avisa a página pai que os dados são válidos utilizando um `EventCallback`.