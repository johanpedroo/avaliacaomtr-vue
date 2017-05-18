<template>
  <header class="topo">
    <BarraPesquisa></BarraPesquisa>
    <Categorias></Categorias>
  </header>
</template>

<script>
  import BarraPesquisa from './BarraPesquisa'
  import Categorias from './Categorias'

  export default {
    name: 'Header',
    data(){
      return {}
    },
    components: {
      BarraPesquisa,
      Categorias
    }
  }
</script>
