<template>
  <div id="app">
    <h1>Тестовое задание</h1>
    <LoadDataJson/>
  </div>
</template>

<script>
import LoadDataJson from './components/LoadDataJson.vue'

export default {
  name: 'App',
  components: {
    LoadDataJson
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
  margin-top: 60px;
}
</style>
