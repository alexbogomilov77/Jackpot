<template>
  <div class="pot-wrapper large">
    <img class="img" :src="imgPath">
    <div class="prize">
      <img class="img" src="@/assets/images/border.png">
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
  name: 'MainPot',
  props: ["sum", "currency", "drop", "image"],
  computed: {
    imgPath: function () {
      return require('@/assets/images/' + this.image + ".png")
    }
  }
}
</script>
