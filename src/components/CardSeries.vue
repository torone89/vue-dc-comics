<template>
  <div class="cards">
    <img :src="serieSrc" />
    <h3>{{ serieTitle }}</h3>
  </div>
</template>


<script>
export default {
  name: "CardSeries",
  props: {
    serieSrc: String,
    serieTitle: String,
  },
};
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style lang= "scss" scoped>
@import "../assets/sass/vars";

// STILE CARDS

.cards {
  margin-top: 30px;
  flex-basis: calc(100% / 6 - 20px);
  padding: 5px;

  img {
    width: 1500px;
    height: 150px;
    cursor: pointer;
    &:hover {
      transition: 0, 3s;
      transform: scale(1);
      opacity: 50%;
    }
  }
  h3 {
    margin-top: 5px;
    color: $lightVhite-color;
    font-size: 15px;
  }
}
</style>
