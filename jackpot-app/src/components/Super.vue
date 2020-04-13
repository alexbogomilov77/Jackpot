<template>
  <div class="box">
    <!-- <img alt="logo" :src="`../assets/images/${image}.png`"> -->
    <!-- <img alt="Vue logo" src="../assets/images/super.png"> -->
    <img alt="Vue logo" :src="imgPath"/>
    <p>{{ type }}</p>
    <p>{{ sum }}</p>
  </div>
</template>

<script>
export default {
  name: 'Super',
  props: ["type", "sum", "currency", "drop", "image"],
  computed: {
    imgPath: function () {
      return require('../assets/' + this.image + '.png')
      // return require("@/assets/images/" + this.image);
    }
  }
}
</script>
