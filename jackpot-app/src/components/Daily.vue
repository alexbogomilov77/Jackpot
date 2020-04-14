<template>
  <div class="box mainBox">
    <img alt="Vue logo" :src="imgPath">
    <div class="daily">
      <img src="@/assets/images/border.png">
      <p>{{currency}} {{ sum }}</p>
    </div>
    <!-- <img src="../assets/images/border.png" alt="border"> -->
    <p>Must drop in {{ drop }}</p>
  </div>
</template>

<script>
export default {
  name: 'Daily',
  props: ["sum", "currency", "drop", "image"],
  computed: {
    imgPath: function () {
      return require('@/assets/images/' + this.image + ".png")
    }
  }
}
</script>
