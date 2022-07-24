<template>
  <header class="container">
    <figure>
      <a href="#"><img src="../assets/img/dc-logo.png" alt="logo"></a>
    </figure>
    <nav class="navbar">
      <ul>
        <li :class="link.current? 'active':'' " v-for="link in links " v-bind:key="link.text">
          <a @click="setActive(link)" :href="link.url">
            {{link.text.toUpperCase()}}
          </a>
        </li>
      </ul>
    </nav>
  </header>
</template>

<script>
export default {
  name: 'MyHeader',
  data: function () {
    return {
      links: [
        {
          text: 'Characters',
          url: '#',
          current: false
        },
        {
          text: 'Comics',
          url: '#',
          current: true
        },
        {
          text: 'Movies',
          url: '#',
          current: false
        },
        {
          text: 'TV',
          url: '#',
          current: false
        },
        {
          text: 'Games',
          url: '#',
          current: false
        },
        {
          text: 'Collectibles',
          url: '#',
          current: false
        },
        {
          text: 'Videos',
          url: '#',
          current: false
        },
        {
          text: 'Fans',
          url: '#',
          current: false
        },
        {
          text: 'News',
          url: '#',
          current: false
        },
        {
          text: 'Shop',
          url: '#',
          current: false
        }
      ]

    }
  },
  methods: {
    setActive (link) {
      this.links.forEach(cur => { cur.current = false })
      link.current = true
    }
  }
}
</script>

<style scoped lang="scss">

img{
  height: 100%;
  max-width: unset;
}
figure{
  height: 80%;
}
.container{
    padding: 0em 8em;
    height: 100px;
    align-items: center;
    justify-content: space-between;
    display: flex;
}
.navbar{
  height: 100%;
}
ul{
    display: flex;
    height: 100%;
}
li{
  border-bottom: 3px solid transparent;
  height: 100%;
  display: flex;
  align-items: center;

}
ul a{
    color: black;
    font-weight: 600;
    font-size: 1em;
    padding: 0 6px;
}
.active{
  border-bottom: 3px solid #0282f6;
  a{
    color: #0282f6;
  }
}
</style>
