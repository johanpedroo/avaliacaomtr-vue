<template>
  <div class="container">
    <section class="produto">
      <Galeria :nome="produto.nome" :fotos="produto.fotos"></Galeria>
      <DetalhesProduto :produto="produto"></DetalhesProduto>
    </section>
  </div>
</template>

<script>
  import DetalhesProduto from './DetalhesProduto'
  import Galeria from './Galeria'
  export default {
    name: 'Produto',
    props: [
      'produto'
    ],
    components: {
      DetalhesProduto,
      Galeria
    }
  }
</script>
