<template>
  <div class="box small">
    <img :src="imgPath" alt="logo">
    <div class="info">
      <p>{{currency}} {{ sum }}</p>
        <span  v-if="drop">
          <i style="font-style:normal">&#128338;</i>
          Must drop in {{ drop }}
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
