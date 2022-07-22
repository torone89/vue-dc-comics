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
          <li>
            <img src="../assets/img/buy-comics-digital-comics.png" alt="" />
            <span>digital comics</span>
          </li>
          <li>
            <img src="../assets/img/buy-comics-merchandise.png" alt="" />
            <span>dc merchandise</span>
          </li>
          <li>
            <img src="../assets/img/buy-comics-subscriptions.png" alt="" />
            <span>subscription</span>
          </li>
          <li>
            <img src="../assets/img/buy-comics-shop-locator.png" alt="" />
            <span>comic shop locator</span>
          </li>
          <li>
            <img src="../assets/img/buy-dc-power-visa.svg" alt="" />
            <span>dc power visa</span>
          </li>
        </ul>
      </div>
    </section>
  </main>
</template>

<script>
export default {
  name: "THeMain",
};
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
/* HEADER */
header {
  background-color: black;
  padding: 50px 0;
}

h1 {
  color: white;
  font-weight: 500;
  font-size: 24px;
}

/* SEcTION ShOP */
.shop {
  background-color: #1e86ed;
  padding: 50px 0;
}

.container ul {
  display: flex;
  justify-content: space-around;
  align-items: center;
  text-transform: uppercase;
}
.container ul li {
  display: flex;
  align-items: center;
  color: white;
  cursor: pointer;
}

img {
  width: 40px;
  margin-right: 15px;
}
</style>