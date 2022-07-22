<template>
  <header>
    <div class="container">
      <nav>
        <figure>
          <img src="@/assets/img/dc-logo.png" alt="" />
        </figure>
        <ul>
          <li><a href="#"></a>Characters</li>
          <li><a href="#"></a>Comics</li>
          <li><a href="#"></a> Movies</li>
          <li><a href="#"></a>Tv</li>
          <li><a href="#"></a>Games</li>
          <li><a href="#"></a>Collectibles</li>
          <li><a href="#"></a>Videos</li>
          <li><a href="#"></a>Fan</li>
          <li><a href="#"></a>News</li>
          <li><a href="#"></a>Shop</li>
        </ul>
      </nav>
    </div>
  </header>
</template>

<script>
export default {
  name: "BaseHeader",
};
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
nav {
  display: flex;
  padding: 20px 0px;
}
figure {
  display: inline-block;
}
ul {
  display: flex;
  justify-content: flex-end;
  align-items: center;
  width: 100%;
}

ul li {
  font-weight: bold;
  padding: 0 15px;
}
</style>
