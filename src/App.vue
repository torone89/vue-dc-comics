<template>
  <div id="app">
    <!-- COMPONENTE HEADER -->
    <BaseHeader />
    <!-- COMPONTENTE MAIN -->
    <TheMain :cards="cards" />
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
import json from "../dc-comics.json";

export default {
  name: "App",
  components: {
    BaseHeader,
    TheMain,
    BaseFooter,
    SocialFooter,
  },
  data() {
    return {
      cards: json,
    };
  },
};
</script>

<style lang="scss">
@import "./assets/sass/style.scss";
@import "./assets/sass/_utils.scss";
</style>