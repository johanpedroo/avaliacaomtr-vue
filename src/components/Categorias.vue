<template>
  <div class="menu">
    <nav class="container categorias">
      <ul>
        <li v-for="valor in categorias">
          <a href="#">{{valor}}</a>
        </li>
      </ul>
    </nav>

  </div>
</template>

<script>
  import categorias from '../categoriaDados'

  export default {
    name: 'Categorias',
    data(){
      return {
        categorias
      }
    }
  }
</script>
