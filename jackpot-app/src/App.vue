<template>
  <div id="app">
    <div class="warning">
      <h3>Screen width should be at least 150px!</h3>
    </div>
    <div class="container">
      <div v-for="(pot) in pots" :key="pot.id">
        <MainPot
          v-if="pot.potType == 'big'"
          :sum="pot.sum"
          :currency="pot.currency"
          :drop="pot.must_drop_in"
          :image="pot.imageType"
        />
        <Pot
          v-else
          :sum="pot.sum"
          :currency="pot.currency"
          :drop="pot.must_drop_in"
          :image="pot.imageType"
        />
      </div>
    </div>
  </div>
</template>

<script>
import json from '@/data/mockData.json';
import MainPot from '@/components/MainPot.vue'
import Pot from '@/components/Pot.vue'

export default {
  name: 'App',
  components: {
    MainPot,
    Pot
  },
  data() {
    return {
      pots: json
    }
  }
}
</script>

