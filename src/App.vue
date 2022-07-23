<template>
  <div>
    <MyHeader></MyHeader>
    <MyContent></MyContent>
    <MyFooter></MyFooter>
  </div>
</template>

<script>
import MyHeader from './components/MyHeader.vue'
import MyContent from './components/MyContent.vue'
import MyFooter from './components/MyFooter.vue'
export default {
  name: 'Dc-comics',
  components: {
    MyHeader,
    MyContent,
    MyFooter
  }
}
</script>

<style>
/* reset */
*{
  margin: 0;
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
.container {
  padding: 2em 8em;
}
</style>
