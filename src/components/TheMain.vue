<template>
  <main>
    <header>
      <div class="container">
        <h1>Content Goes Here</h1>
      </div>
    </header>

    <section class="shop">
      <div class="container">
        <ul>
          <li v-for="(shop, index) in shop" :key="index">
            <img :src="require(`../assets/img/${shop.src}`)" :alt="shop.text" />
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
  }
}

img {
  width: 40px;
  margin-right: 15px;
}
</style>