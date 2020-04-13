<template>
  <div id="app">
    <div class="container">
      <div v-for="(pot) in pots" :key="pot.id">
        <!-- <Daily
          v-if="pot.potType == 'big'"
          :type="pot.type"
          :sum="pot.sum"
          :currency="pot.currency"
          :drop="pot.drop"
          :image="pot.image"
        /> -->
        <Super
          :type="pot.potType"
          :sum="pot.sum"
          :currency="pot.currency"
          :drop="pot.drop"
          :image="pot.imageType"
        />
      </div>
    </div>
  </div>
</template>

<script>
import json from '@/data/mockData.json';
// import Daily from '@/components/Daily.vue'
import Super from '@/components/Super.vue'

export default {
  name: 'App',
  components: {
    // Daily,
    Super
  },
  data() {
    return {
      pots: json
    }
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
