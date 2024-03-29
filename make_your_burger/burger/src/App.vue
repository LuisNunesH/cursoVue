<script>
import NavBar from "./components/NavBar.vue";
import Footer from "./components/Footer.vue";

export default {
  components: {
    NavBar,
    Footer,
  },
  data() {
    return{
      logo_src: "/img/logo.png",
      app_name: "Make Your Burger"
    }
  }
};
</script>

<template>
  <NavBar :logo="logo_src" :alt="app_name" />
  <RouterView />
  <Footer />
</template>

<style scoped>
</style>
