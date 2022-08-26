<template>
  <div class="main">
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

.main {
  max-width: 1536px;
  width: 80%;
  margin: 0 auto;
  padding: 50px 0;

  input{
    border: 1px solid #000;
    background: #fff;
    margin-right: 50px;
  }

  button{
    padding: 5px 20px;
    border-radius: 20px;
    background-color: rgb(40, 174, 130);
    color: #fff;
    font-weight: 600;
  }

}

</style>
