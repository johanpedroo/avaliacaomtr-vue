<template>
  <div id="app">
    <HeaderBp></HeaderBp>
    <ContentBp></ContentBp>
  </div>
</template>

<script>
  import HeaderBp from './components/Header'
  import ContentBp from './components/Content'
  import 'normalize.css';
  import './assets/css/App.css'

  export default {
    name: 'App',
    components: {
      HeaderBp,
      ContentBp
    }
  }
</script>

<style>
</style>
