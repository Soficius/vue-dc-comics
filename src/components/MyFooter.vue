<template>
  <footer>
    <div class="container">
      <div class="flex-row">
        <div class="flex-c-col">
          <h3>DC Comics</h3>
          <ul>
            <li v-for="comic in dcComics" v-bind:key="comic[i]">
              <a href="#">{{ comic }}</a>
            </li>
          </ul>
          <h3>Shop</h3>
          <ul>
            <li v-for="shop in shops" v-bind:key="shop[i]">
              <a href="#">{{ shop }}</a>
            </li>
          </ul>
        </div>
        <div class="flex-c-col">
          <h3>DC</h3>
          <ul>
            <li v-for="dc in dcs" v-bind:key="dc[i]">
              <a href="#">{{ dc }}</a>
            </li>
          </ul>
        </div>
        <div class="flex-c-col">
          <h3>Sites</h3>
          <ul>
            <li v-for="site in sites" v-bind:key="site[i]">
              <a href="#">{{ site }}</a>
            </li>
          </ul>
        </div>
      </div>
    </div>
    <div class="logo-bg"></div>
  </footer>
</template>
<script>
export default {
  name: 'MyFooter',
  data: function () {
    return {
      dcComics: ['characters', 'comics', 'movies', 'tv', 'games', 'vodeos', 'news'],
      shops: ['shop DC', 'shop DC', 'collectibles'],
      dcs: ['term of use', 'privacy policy (new)', 'ad choices', 'advertising', 'jobs', 'subscriptions', 'talent workshops', 'cpsc certificates ', 'ratings', 'shop help', 'contact us'],
      sites: ['DC', 'mad magazine', 'dc kids', 'dc universe', 'dc power visa']

    }
  }
}
</script>
<style scoped>
footer{
  min-height: 400px;
  background-image: url(../assets/img/footer-bg.jpg);
  background-repeat: no-repeat;
  background-size: cover;
  color: white;
  justify-content: space-between;
    display: flex;
}
.container{
  padding-right: 0;
    width: 50%;
}
a{
  color: gray;
}
.flex-row{
  display: flex;
}
.flex-c-col{
  display: flex;
  flex-direction: column;
  padding: 0 1em;
}
ul li{
  padding: 2px 0;
}
.logo-bg{
  width: 40%;
  background-image: url(../assets/img/dc-logo-bg.png);
  background-position: center;
  background-size: cover;
}

</style>
