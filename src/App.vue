<template>
  <div id="app">
    <!-- COMPONENTE HEADER -->
    <BaseHeader />
    <!-- Componente JUMBOTRON -->
    <TheJumbotron />
    <!-- COMPONTENTE MAIN -->
    <TheMain :cards="cards" />
    <!-- COMPONENTE FOOTER -->
    <BaseFooter />
    <!-- COMPONENTE FOOTER -->
    <SocialFooter />
  </div>
</template>

<script>
import TheJumbotron from "./components/TheJumbotron.vue";
import BaseHeader from "./components/BaseHeader.vue";
import TheMain from "./components/TheMain.vue";
import BaseFooter from "./components/BaseFooter.vue";
import SocialFooter from "./components/SocialFooter.vue";

// IMPORTO I DATI da dc-comics.json
import json from "../dc-comics.json";

export default {
  name: "App",
  components: {
    BaseHeader,
    TheJumbotron,
    TheMain,
    BaseFooter,
    SocialFooter,
  },
  data() {
    // RICHIAMO I DATI DAL FILE JSON dc-comics
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