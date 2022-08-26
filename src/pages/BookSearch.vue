<template>
  <div>
    <input
    v-model="keyword"
    class="serchEnter"
    type="text">
    <button @click="getSearchResults()">検索</button>
  </div>
</template>

<script>
import axios from 'axios'
export default {
  // name: BookSearch,
  data () {
    return {
      keyword: '',
      searchResulys: []
    }
  },
  methods: {
    getSearchResults () {
      axios.get(`https://www.googleapis.com/books/v1/volumes?q=${this.keyword}`)
        .then(res => {
          if (res.data) {
            this.result = res.data
            console.log(this.result)
          }
        })
        .catch(err => {
          console.error(err)
        })
    }
  }
}
</script>

<style lang="scss" scoped>
</style>
