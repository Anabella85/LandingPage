<template>
  <div id="app">
    <Header />
    <About id="about" />
    <img class="background-home" src="./assets/rectangle.svg" />
    <Portfolio id="portfolio" />
    <TestimonialsClients id="testimonials" />
    <Footer />
  </div>
</template>

<script>
import Header from "./components/Header.vue";
import About from "./components/About.vue";
import Portfolio from "./components/Portfolio.vue";
import TestimonialsClients from "./components/TestimonialsClients.vue";
import Footer from "./components/Footer.vue";
export default {
  name: "App",
  components: {
    Header,
    About,
    Portfolio,
    TestimonialsClients,
    Footer,
  },
};
</script>

<style>
body {
  scroll-behavior: smooth;
  overflow-x: hidden;
}
button {
  outline: none;
  color: white;
  box-shadow: none;
}
#app {
  font-family: "Livvic";
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
}
.background-home {
  position: absolute;
  top: 0px;
  right: 0px;
  z-index: -1;
}
</style>
