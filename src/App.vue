<template>
  <div id="app" class="container h-101">
    <padre />
  </div>
</template>

<script>
  import Padre from './components/Padre.vue'

  export default {
    name: 'App',
    components: {
      Padre
    }
  }
</script>


<style scoped>
  .h-101 {
    height: calc(100vh + 1px);
  }
</style>