<template>
  <main>
    <!-- SEZIONE CARDS -->
    <section class="card-section">
      <div class="container">
        <!-- BUTTON CURRENT SERIES -->
        <div class="button-load">
          <button>Current series</button>
        </div>

        <!-- LOgica Card -->
        <div class="cards-box">
          <!-- COMPONENTE CARD + LOGICA CREAZIONE CARD -->
          <CardSeries
            v-for="(card, index) in cards"
            :key="index"
            :showCard="card"
            :serieSrc="card.thumb"
            :serieTitle="card.series"
          />
        </div>
        <!-- BUTTON LOAD -->
        <div class="button-load">
          <button>load more</button>
        </div>
      </div>
    </section>

    <!-- SEZIONE SHOP -->
    <section class="shop">
      <div class="container">
        <ul>
          <!-- LOGICA SHOP -->
          <li v-for="shop in shop" :key="shop">
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
      // DATI SEZIONE SHOP
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

/* HEADER */
header {
  background-color: black;
  padding: 50px 0;
}

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

.cards-box {
  margin: 0 auto;
  display: flex;
  justify-content: space-between;
  flex-wrap: wrap;
}
// BUTTON LOAD STYLE// + CUrrentSeries (provvisorio)
.button-load {
  padding-bottom: 30px;
  text-align: center;

  button {
    background-color: $blue-color;
    padding: 15px 50px;
    margin: 0 auto;
    color: $lightVhite-color;
    text-transform: uppercase;
    font-weight: bold;
    font-size: 15px;
    border: 1px solid transparent;
    cursor: pointer;

    &:hover {
      background-color: $lightVhite-color;
      color: black;
      border: 1px solid black;
    }
  }
}
</style>

