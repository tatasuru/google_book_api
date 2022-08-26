<template>
  <div class="footer">

      <router-link class="footerbtn" to="/">BookIndex</router-link>
      <router-link class="footerbtn" to="/search">BookSearch</router-link>
      <router-link class="footerbtn" to="/edit">BookEdit</router-link>
      <router-link class="headerbtn" to="/weather">Weather</router-link>

      <v-spacer></v-spacer>

  </div>
</template>

<script>
export default {
  name: 'C_Footer',
  data () {
    return {}
  }
}
</script>

<style lang="scss" scoped>

.footer{
  padding: 50px;
  background: #2776d2;
}

.footerbtn{
  color: #fff;
  margin-right: 50px;
  text-decoration: none;
  font-size: 20px;
}
</style>
