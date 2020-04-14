<template>
  <div class="box small">
    <img class="img" :src="imgPath" alt="logo">
    <div class="info">
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
  name: 'Super',
  props: ["sum", "currency", "drop", "image"],
  computed: {
    imgPath: function () {
      return require('@/assets/images/' + this.image + ".png")
    }
  }
}
</script>
