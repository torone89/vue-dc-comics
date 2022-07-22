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

<style lang="scss">
@import "./assets/sass/style.scss";
@import "./assets/sass/_utils.scss";
</style>