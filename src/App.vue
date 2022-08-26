<template>
  <v-app>
    <Header />
    <v-main>
      <nav>
        <router-link to="/">BookIndex</router-link> |
        <router-link to="/search">BookSearch</router-link> |
        <router-link to="/edit">BookEdit</router-link> |
      </nav>
      <transition mode="out-in">
      <router-view/>
      </transition>
    </v-main>
    <Footer />
  </v-app>
</template>

<script>
import Header from './global/C_Header.vue'
import Footer from './global/C_Footer.vue'

export default {
  name: 'App',
  data () {
    return {}
  },
  components: {
    Header,
    Footer
  }
}
</script>

<style lang="scss" scoped>

.v-enter-active, .v-leave-active {
  transition: opacity .5s;
}
.v-enter, .v-leave-to {
  opacity: 0;
}

</style>
