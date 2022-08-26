<template>
  <div>

    <v-app-bar
      app
      color="primary"
      dark
      class="header"
    >
      <router-link class="headerbtn" to="/">BookIndex</router-link>
      <router-link class="headerbtn" to="/search">BookSearch</router-link>
      <router-link class="headerbtn" to="/edit">BookEdit</router-link>
      <router-link class="headerbtn" to="/weather">Weather</router-link>

      <v-spacer></v-spacer>

    </v-app-bar>

  </div>
</template>

<script>
export default {
  name: 'C_Header',
  data () {
    return {}
  }
}
</script>

<style lang="scss" scoped>

.header{
  padding: 0 50px;
}

.headerbtn{
  color: #fff;
  margin-right: 50px;
  text-decoration: none;
  font-size: 20px;
}

</style>
