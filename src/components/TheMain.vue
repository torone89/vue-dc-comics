<template>
  <main>
    <header>
      <div class="container">
        <h1>Content Goes Here</h1>
      </div>
    </header>
    <section class="card-section">
      <div class="container">
        <div class="button-load">
          <button>Current series</button>
        </div>

        <div class="cards-box">
          <div v-for="(card, index) in cards" :key="index" class="cards">
            <img :src="card.thumb" />
            <h3>{{ card.series }}</h3>
          </div>
        </div>

        <div class="button-load">
          <button>load more</button>
        </div>
      </div>
    </section>
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
export default {
  name: "THeMain",
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
  props: {
    cards: Array,
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