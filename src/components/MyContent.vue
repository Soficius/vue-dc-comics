<template>
  <main>
    <BooksCards :books="comics"/>
  </main>
</template>
<script>
import axios from 'axios'
import BooksCards from './BooksCards.vue'
export default {
  name: 'MyContent',
  data: function () {
    return {
      comics: []
    }
  },
  mounted () {
    axios.get('./dc-comics.json').then((res) => {
      this.comics = res.data
    })
  },
  components: {
    BooksCards
  }
}
</script>
<style lang="scss" scoped>
main{
  background-color: black;
  min-height: 100px;
}
</style>
