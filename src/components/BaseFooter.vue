<template>
  <footer>
    <div class="container">
      <nav>
        <div class="nav-left">
          <ul>
            <li><h3>dc comics</h3></li>
            <li><a href="#">Characters</a></li>
            <li><a href="#">Comics</a></li>
            <li><a href="#">Movies</a></li>
            <li><a href="#">Tv</a></li>
            <li><a href="#">Games</a></li>
            <li><a href="#">Videos</a></li>
            <li><a href="#">News</a></li>
            <li><h3>shop</h3></li>
            <li><a href="#">Shop DC</a></li>
            <li><a href="#">Shop DC Collectibles</a></li>
          </ul>

          <ul>
            <li><h3>dc</h3></li>
            <li><a href="#">Terms Of Use</a></li>
            <li><a href="#">Privacy policy (New)</a></li>
            <li><a href="#">Ad Choices</a></li>
            <li><a href="#">Advertising</a></li>
            <li><a href="#">Jobs</a></li>
            <li><a href="#">Subscriptions</a></li>
            <li><a href="#">Talent Workshops</a></li>
            <li><a href="#">CPSC Certificates</a></li>
            <li><a href="#">Ratings</a></li>
            <li><a href="#">Shop Help</a></li>
            <li><a href="#">Contact Us</a></li>
          </ul>

          <ul>
            <li><h3>sites</h3></li>
            <li><a href="#">DC</a></li>
            <li><a href="#">MAD Magazine</a></li>
            <li><a href="#">DC Kids</a></li>
            <li><a href="#">DC Universe</a></li>
            <li><a href="#">DC Power Visa</a></li>
          </ul>
        </div>

        <div class="nav-right">
          <figure>
            <img src="../assets/img/dc-logo-bg.png" alt="" />
          </figure>
        </div>
      </nav>
    </div>
  </footer>
</template>

<script>
export default {
  name: "BaseFooter",
};
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style lang= "scss" scoped>
@import "../assets/sass/vars";
footer {
  background-image: url("../assets/img/footer-bg.jpg");
  background-size: cover;
}
nav {
  display: flex;
  justify-content: space-between;
}
.nav-left {
  display: flex;
  padding: 40px 0;
  li {
    margin-right: 30px;
    line-height: 30px;
  }
}

h3 {
  text-transform: uppercase;
  font-size: 19px;
  color: $lightVhite-color;
}
a {
  text-decoration: none;
  color: grey;
}
.nav-right {
  max-height: 450px;
  overflow: hidden;

  img {
    margin-top: -50px;
  }
}
</style>



