<template>
  <footer class="social-bg">
    <div class="container">
      <div class="social">
        <!-- BOTTONE -->
        <div class="sign-up">
          <button><a href="#">sign-up now!</a></button>
        </div>
        <!-- SOCIAL ICONS -->
        <div class="social-icons">
          <span class="follow">follow us</span>
          <img src="../assets/img/footer-facebook.png" alt="" />
          <img src="../assets/img/footer-twitter.png" alt="" />
          <img src="../assets/img/footer-youtube.png" alt="" />
          <img src="../assets/img/footer-pinterest.png" alt="" />
          <img src="../assets/img/footer-periscope.png" alt="" />
        </div>
      </div>
    </div>
  </footer>
</template>

<script>
export default {
  name: "SocialFooter",
};
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
.social-bg {
  background-color: #2f2f2f;
}

.social {
  display: flex;
  justify-content: space-between;
  align-items: center;
  padding: 30px;
}
.social-icons {
  display: flex;
  justify-content: space-around;
}

.sign-up {
  margin-left: 5px;
}

/* BUTTON */
button {
  border: none;
  border: 2px solid #1e86ed;
  padding: 17px;
  background-color: #2f2f2f;
}

/* ALINK */
a {
  text-transform: uppercase;
  font-weight: bold;
  color: white;
  font-size: 15px;
}

/* IMG */
img {
  padding: 10px;
  width: 50px;
  height: 50px;
  cursor: pointer;
}

img:hover {
  background-color: white;
  border-radius: 50px 50px;
}

/* SPAN FOLLOW */
.follow {
  text-transform: uppercase;
  color: #1e86ed;
  font-weight: bold;
  font-size: 20px;
  margin: 15px 10px;
  cursor: pointer;
}
</style>