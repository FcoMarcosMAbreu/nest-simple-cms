# Classes do nosso CMS

```plantuml
class Cliente {
  - id: int
  - nome: string
  - endereco: string
  - carrinho: Carrinho
  + adicionarAoCarrinho(item: Item): void
  + realizarPedido(): Pedido
}

class Produto {
  - id: int
  - nome: string
  - descricao: string
  - preco: float
}

class Carrinho {
  - itens: List<Item>
  + adicionarItem(produto: Produto, quantidade: int): void
  + removerItem(item: Item): void
  + calcularTotal(): float
}

class Item {
  - produto: Produto
  - quantidade: int
  + calcularSubtotal(): float
}

class Pedido {
  - id: int
  - cliente: Cliente
  - itens: List<Item>
  - status: string
  - total: float
  + calcularTotal(): float
  + confirmarPedido(): void
}

class Estoque {
  - produtos: List<Produto>
  + adicionarProduto(produto: Produto): void
  + removerProduto(produto: Produto): void
  + atualizarEstoque(produto: Produto, quantidade: int): void
}
```

## Blog Simples

```plantuml
class User {
  - id: uuid
  - email: string
  + postArticle(): void
  + editArticle(): void
  + deleteArticle(): void
  + addComment(): void
  + editComment(): void
  + deleteComment(): void
}

class Article {
  - id: uuid
  - title: string
  - description: string
  - author: User.id
  - publishDateTime: TimeStamp
  - content: string
}

class Comment {
  - id: uuid
  - article: Article.id
  - author: User.id
  - publishDateTime: TimeStamp
  - content: string
}


```