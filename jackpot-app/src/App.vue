<template>
  <div id="app">
    <div class="container">
      <Daily/>
      <Hourly/>
      <Super/>
    </div>
  </div>
</template>

<script>
import json from '@/data/mockData.json';
import Hourly from '@/components/Hourly.vue'
import Daily from '@/components/Daily.vue'
import Super from '@/components/Super.vue'

export default {
  name: 'App',
  components: {
    Hourly,
    Daily,
    Super
  },
  mounted() {
    console.log(json)
  }
}
</script>

<style lang="scss">
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
