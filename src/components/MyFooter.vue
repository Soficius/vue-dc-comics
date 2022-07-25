<template>
  <footer>
    <div class="outer-footer">
      <div class="container half">
        <div class="flex-row">
          <div class="flex-c-col">
            <h3>DC Comics</h3>
            <ul>
              <li v-for="(comic,i) in dcComics" v-bind:key="'comic-'+i">
                <a href="#">{{ comic }}</a>
              </li>
            </ul>
            <h3>Shop</h3>
            <ul>
              <li v-for="(shop,i) in shops" v-bind:key="'shop-'+i">
                <a href="#">{{ shop }}</a>
              </li>
            </ul>
          </div>
          <div class="flex-c-col">
            <h3>DC</h3>
            <ul>
              <li v-for="(dc,i) in dcs" v-bind:key="'dc-'+i">
                <a href="#">{{ dc }}</a>
              </li>
            </ul>
          </div>
          <div class="flex-c-col">
            <h3>Sites</h3>
            <ul>
              <li v-for="(site,i) in sites" v-bind:key="'site-'+i">
                <a href="#">{{ site }}</a>
              </li>
            </ul>
          </div>
        </div>
      </div>
      <div class="logo-bg"></div>
    </div>
    <div class="inner-footer">
      <div class="container">
        <div class="flex-row justify-between">
          <a class="subscribe">SIGN-UP NOW!</a>
          <div class="social flex-row">
            <a class="pad-lr" href="#">FOLLOW US</a>
            <figure v-for="(social,i) in socials" class="pad-lr" :key="'social-'+i">
              <img :src="'img/'+ social" alt="social">
            </figure>
          </div>
        </div>
      </div>
    </div>
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
      sites: ['DC', 'mad magazine', 'dc kids', 'dc universe', 'dc power visa'],
      socials: ['footer-facebook.png', 'footer-periscope.png', 'footer-pinterest.png', 'footer-twitter.png', 'footer-youtube.png']

    }
  }
}
</script>
<style lang="scss" scoped>
.subscribe {
  border: 3px solid #0282f6;
  align-items: center;
  color: white;
  display: flex;
}

.social {
  align-items: center;
}

.social a {
  color: #0282f6;

}

.pad-lr {
  padding: 0px 4px
}

.justify-between {
  justify-content: space-between;
}

footer {
  color: white;
}

.outer-footer {
  min-height: 413px;
  background-image: url(../assets/img/footer-bg.jpg);
  background-repeat: no-repeat;
  background-size: cover;
  display: flex;
  justify-content: space-between;
}

.inner-footer {
  height: 100px;
  width: 100%;
  background-color: #303030;
}

.container.half {
  padding-right: 0;
  width: 50%;
}

a {
  color: gray;
}

.flex-row {
  display: flex;
}

.flex-c-col {
  display: flex;
  flex-direction: column;
  padding: 0 1em;
}

ul li {
  padding: 2px 0;
}

.logo-bg {
  width: 40%;
  background-image: url(../assets/img/dc-logo-bg.png);
  background-position: center;
  background-size: cover;
}
</style>
