<template>
  <section class="jumbo"></section>
</template>

<script>
export default {
  name: "TheJumbotron",
};
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style lang= "scss" scoped>
@import "../assets/sass/vars";

.jumbo {
  height: 400px;
  background-image: $img-jumbo;
  background-size: cover;
}
</style>