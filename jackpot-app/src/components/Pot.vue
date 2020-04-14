<template>
  <div class="pot-wrapper small">
    <img class="img" :src="imgPath">
    <div class="prize">
      <p class="sum">{{currency}}{{ sum }}</p>
      <span class="drop" v-if="drop">
        Must drop in
        <i class="icon">&#128338;</i>
        {{ drop }}
      </span>
    </div>
  </div>
</template>

<script>
export default {
  name: 'Pot',
  props: ["sum", "currency", "drop", "image"],
  computed: {
    imgPath: function () {
      return require(`@/assets/images/${this.image}.png`)
    }
  }
}
</script>
