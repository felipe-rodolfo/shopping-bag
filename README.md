# Aplicativo de Compras Vue.js

Esta aplicação Vue.js serve como uma plataforma de compras, onde os usuários podem explorar e adicionar produtos ao carrinho de compras.

## Sumário
- [Navegação](#navegação)
- [Página Inicial](#página-inicial)
- [Carrinho de Compras](#carrinho-de-compras)
- [VueX Store](#vuex-store)
- [Router](#router)

## Navegação

A barra de navegação, localizada no topo da página, fornece fácil acesso a diferentes seções da aplicação. Os usuários podem navegar entre a página inicial e o carrinho de compras.

```html
<div id="nav">
  <router-link to="/">Início</router-link> -
  <router-link to="/basket">Carrinho de Compras {{ this.productsInBag.length  }}</router-link> 
</div>
```

## Página Inicial

A página inicial exibe uma coleção de produtos que os usuários podem explorar. Cada produto inclui uma imagem, título, preço e uma opção para adicioná-lo ao carrinho de compras.

```html
<div class="home">
  <div class="products">
    <!-- Componentes de produtos -->
  </div>
</div>
```

## Carrinho de Compras

A página do carrinho de compras lista os itens que os usuários adicionaram. Eles podem gerenciar a quantidade e remover itens do carrinho.

```html
<div class="basket">
  <div class="items">
    <!-- Itens do carrinho de compras -->
  </div>
</div>
```

## VueX Store

A store VueX gerencia o estado para produtos e o carrinho de compras. Inclui mutações para carregar produtos, adicionar/remover do carrinho e carregar o carrinho do armazenamento local.

```javascript
// VueX Store
state: {
  products: [],
  productsInBag: []
},
mutations: {
  // Mutations para carregar produtos e gerenciar o carrinho
},
actions: {
  // Actions para carregar produtos e gerenciar o carrinho
}
```

## Router

O router gerencia a navegação entre a página inicial e o carrinho de compras.

```javascript
// Vue Router
const routes = [
  {
    path: '/',
    name: 'Home',
    component: Home
  },
  {
    path: '/basket',
    name: 'Basket',
    component: Basket
  },
]

const router = createRouter({
  history: createWebHashHistory(),
  routes
})
```

Sinta-se à vontade para explorar e aprimorar ainda mais a aplicação! Se tiver dúvidas ou sugestões, não hesite em entrar em contato. 🚀✨