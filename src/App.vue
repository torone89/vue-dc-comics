<template>
  <div id="app">
    <!-- COMPONENTE HEADER -->
    <BaseHeader />
    <!-- COMPONTENTE MAIN -->
    <TheMain />
    <!-- COMPONENTE FOOTER -->
    <BaseFooter />
    <!-- COMPONENTE FOOTER -->
    <SocialFooter />
  </div>
</template>

<script>
import BaseHeader from "./components/BaseHeader.vue";
import TheMain from "./components/TheMain.vue";
import BaseFooter from "./components/BaseFooter.vue";
import SocialFooter from "./components/SocialFooter.vue";
export default {
  name: "App",
  components: {
    BaseHeader,
    TheMain,
    BaseFooter,
    SocialFooter,
  },
};
</script>

<style>
/* GENERICS */
* {
  margin: 0;
  padding: 0;
  box-sizing: border-box;
}

body {
  font-family: Avenir, Helvetica, Arial, sans-serif;
}

img {
  height: auto;
  max-width: 100%;
}

ul {
  list-style-type: none;
}

a {
  color: black;
  text-decoration: none;
}

/* UTILS */
.container {
  max-width: 1200px;
  margin: 0 auto;
}
</style>
