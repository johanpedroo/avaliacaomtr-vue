<template>
  <div class="container">
    <section class="cards">
      <Card :card="value" :key="i" v-for="(value,i) in cards"/>
    </section>
  </div>
</template>

<script>
  import Card from './Card'
  import cards from '../cardDados'
  export default {
    name: 'Cards',
    data(){
      return {
        cards
      }
    },
    components: {
      Card
    }
  }
</script>
