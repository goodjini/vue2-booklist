<template>
  <div>
    <h1>本の一覧</h1>
    <ul>
      <ui 
        @click="showBookDetail(book.id)"
        v-for="book in books" :key="book.id">
          {{ book.title }}
      </ui>
    </ul>
  </div>
</template>

<script>
export default {
  name: 'BookList',
  data() {
    return {
      bookIndex: -1,
      books: [
        {id:1, title:'タイトル１', content:'本の内容１'},
        {id:2, title:'タイトル２', content:'本の内容２'},
        {id:3, title:'タイトル３', content:'本の内容３'}
      ]
    }
  },
  methods: {
    showBookDetail(id) {
      this.bookIndex = id - 1;
      console.log(this.bookIndex);
      this.$router.push({
        name:'Book',
        params:{
          id: this.books[this.bookIndex].id,
          title: this.books[this.bookIndex].title,
          content: this.books[this.bookIndex].content,
        }
      })
    }
  }

}
</script>

<style>

</style>