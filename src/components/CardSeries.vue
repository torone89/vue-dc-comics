<template>
  <div class="cards-box">
    <div v-for="card in cards" :key="card" class="cards">
      <img :src="card.thumb" />
      <h3>{{ card.series }}</h3>
    </div>
  </div>
</template>


<script>
export default {
  name: "CardSeries",
  props: {
    cards: Array,
  },
};
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style lang= "scss" scoped>
@import "../assets/sass/vars";
.cards-box {
  margin: 0 auto;
  display: flex;
  justify-content: space-between;
  flex-wrap: wrap;

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
    }
  }
}
</style>
