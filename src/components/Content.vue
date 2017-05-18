<template>
  <main class="content">
    <Breadcrumbs :categorias="produto.categorias" :nome="produto.nome"></Breadcrumbs>
    <Produto :produto="produto"></Produto>
    <Cards></Cards>
  </main>
</template>

<script>
  import Breadcrumbs from './Breadcrumbs'
  import Produto from './Produto'
  import Cards from './Cards'
  import produto from '../produtoDados'

  export default {
    name: 'Content',
    data(){
      return {
        produto
      }
    },
    components: {
      Breadcrumbs,
      Produto,
      Cards
    }
  }
</script>
