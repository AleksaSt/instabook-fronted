<template>
  <div style="background-color: rgba(var(--b3f,250,250,250),1)">
    <Navbar v-if="!isLogin"/>
    <router-view/>
    <!-- <Footer/> -->
  </div>
</template>

<script>
// import Footer from './components/Footer.vue'
import Navbar from './components/Navbar.vue'

export default {
  name: 'App',
  components: {
    Navbar,
    // Footer
  },
  computed: {
    isLogin() {
      return this.$route.name === 'Login'
    }
  }
}

</script>

<style scoped>

</style>
