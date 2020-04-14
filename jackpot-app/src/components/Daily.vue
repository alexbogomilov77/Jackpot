<template>
  <div class="box large">
    <img class="img" :src="imgPath">
    <div class="jackpot">
      <img src="@/assets/images/border.png">
      <p class="sum">{{currency}}{{ sum }}</p>
    </div>
    <span class="drop">
      Must drop in
      <i class="icon">&#128338;</i>
      {{ drop }}
    </span>
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
