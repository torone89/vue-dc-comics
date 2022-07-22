<template>
  <header>
    <div class="container">
      <nav>
        <figure>
          <img src="@/assets/img/dc-logo.png" alt="" />
        </figure>
        <!-- LOGICA DINAMICA LISTE -->
        <ul>
          <li
            v-for="(link, index) in links"
            :key="index"
            :class="{ active: link.current }"
          >
            <a :href="link.url">{{ link.text }}</a>
          </li>
        </ul>
      </nav>
    </div>
  </header>
</template>

<script>
export default {
  name: "BaseHeader",
  data() {
    return {
      links: [
        {
          text: "Characters",
          url: "#",
          current: false,
        },
        {
          text: "Comics",
          url: "#",
          current: true,
        },
        {
          text: "Movies",
          url: "#",
          current: false,
        },
        {
          text: "TV",
          url: "#",
          current: false,
        },
        {
          text: "Games",
          url: "#",
          current: false,
        },
        {
          text: "Collectibles",
          url: "#",
          current: false,
        },
        {
          text: "Videos",
          url: "#",
          current: false,
        },
        {
          text: "Fans",
          url: "#",
          current: false,
        },
        {
          text: "News",
          url: "#",
          current: false,
        },
        {
          text: "Shop",
          url: "#",
          current: false,
        },
      ],
    };
  },
};
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style lang= "scss" scoped>
@import "../assets/sass/vars";
nav {
  display: flex;
}

figure {
  display: inline-block;

  img {
    padding: 20px 0px;
  }
}

ul {
  display: flex;
  justify-content: flex-end;
  align-items: center;
  width: 100%;

  li {
    font-weight: bold;
    padding: 0 15px;
    height: 100%;
    text-transform: uppercase;
    cursor: pointer;
    display: flex;
    align-items: center;
    &:hover {
      color: $blue-color;
      border-bottom: 5px solid $blue-color;
    }
  }
}

a {
  color: $strongGray-color;
}
</style>
