<template>
  <div>
    <MyHeader></MyHeader>
    <main></main>
    <footer></footer>
  </div>
</template>

<script>
import MyHeader from './components/MyHeader.vue'
export default {
  name: 'Dc-comics',
  components: {
    MyHeader
  }
}
</script>

<style>
/* reset */
*{
  margin: 0 auto;
  padding: 0;
  box-sizing: border-box;
}
img{
  max-width: 100%;
}
a{
  text-decoration: none;
}
ul{
  list-style-type: none;
}
</style>
