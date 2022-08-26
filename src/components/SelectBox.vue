<template>
  <select
  v-model="SelectedVal">
    <option disabled value="">選択してください</option>
    <option
    v-for="item in items"
    :key="item"
    :value="name === 'a' ? item.name : item.id"
    >{{item.name}}</option>
  </select>
</template>

<script>
export default {
  name: 'SelectBox',
  data () {
    return {
      SelectedVal: ''
    }
  },
  props: {
    items: {
      type: Object
    },
    name: {
      type: String
    }
  },
  watch: {
    SelectedVal (newVal, oldVal) {
      this.$emit('koike', newVal)
    }
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped lang="scss">
select{
  padding: 10px;
  border: 1px solid #000;
  background: #fff;
}
h3 {
  margin: 40px 0 0;
}
ul {
  list-style-type: none;
  padding: 0;
}
li {
  display: inline-block;
  margin: 0 10px;
}
a {
  color: #42b983;
}
</style>
