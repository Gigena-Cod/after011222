<template>
  <div id="app" class="p-12 bg-black">
      <CardlistComponent/>
    </div>
</template>

<script>
import CardlistComponent from './components/CardList.vue'

export default {
  name: 'App',
  components: {
    CardlistComponent
  }
}
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
}
</style>
