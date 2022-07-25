<template>
  <main>
    <!-- SEZIONE CARDS -->
    <section class="card-section">
      <CardSeries :cards="cards" />
    </section>

    <!-- SEZIONE SHOP -->
    <section class="shop">
      <div class="container">
        <ul>
          <li v-for="(shop, index) in shop" :key="index">
            <a href="">
              <img
                :src="require(`../assets/img/${shop.src}`)"
                :alt="shop.text"
              />
            </a>
            <span> {{ shop.text }}</span>
          </li>
        </ul>
      </div>
    </section>
  </main>
</template>

<script>
import CardSeries from "./CardSeries.vue";
export default {
  name: "TheMain",
  components: { CardSeries },
  props: {
    cards: Array,
  },
  data() {
    return {
      shop: [
        {
          text: "Digital Comics",
          src: "buy-comics-digital-comics.png",
          url: "#",
        },
        {
          text: "DC Merchandise",
          src: "buy-comics-merchandise.png",
          url: "#",
        },
        {
          text: "Subscription",
          src: "buy-comics-subscriptions.png",
          url: "#",
        },
        {
          text: "Shop Location",
          src: "buy-comics-shop-locator.png",
          url: "#",
        },
        {
          text: "Dc Power Visa",
          src: "buy-dc-power-visa.svg",
          url: "#",
        },
      ],
    };
  },
};
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style lang= "scss" scoped>
@import "../assets/sass/vars";

h1 {
  color: $lightVhite-color;
  font-weight: 500;
  font-size: 24px;
}

/* SEcTION ShOP */
.shop {
  background-color: $blue-color;
  padding: 50px 0;
}

.container ul {
  display: flex;
  justify-content: space-around;
  align-items: center;
  text-transform: uppercase;
  li {
    display: flex;
    align-items: center;
    color: $lightVhite-color;
    cursor: pointer;
    img {
      width: 40px;
      margin-right: 15px;
    }
  }
}

// CARDS SECTION
.card-section {
  background-color: $CardBgGray-color;
}
</style>