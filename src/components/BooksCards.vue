<template>
  <div class="container box">
    <div v-for="(book, i) in books" :key="'book-' + i" class="card">
      <img :src="book.thumb" alt="" />
      <h3>{{book.series}}</h3>
    </div>
  </div>
</template>

<script>
export default {
  name: 'BooksCards',
  props: {
    books: Array
  }
}
</script>

<style lang="scss" scoped>
.box {
  display: flex;
  flex-wrap: wrap;
  .card {
    flex-basis: calc(100%/6);
    border: 1em solid transparent;
    h3 {
      color: white;
    }
  }
}
</style>
