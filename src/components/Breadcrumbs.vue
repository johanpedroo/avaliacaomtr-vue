<template>
  <nav class="breadcrumbs">
    <div class="container">
      <a href="#" class="breadcrumbs-links">Início</a>
        <span v-for="value in categorias">
          <span class="breadcrumbs-separador">»</span>
          <a href="#" class="breadcrumbs-links">{{value}}</a>
        </span>
      <span class="breadcrumbs-separador">»</span>
      <span>{{nome}}</span>
    </div>
  </nav>
</template>

<script>
  export default {
    name: 'Bradcrumbs',
    props: [
      'categorias',
      'nome'
    ]
  }
</script>
