<template>
<div>
<div id="home">
  <Navbar/>
  <Header/>
  <Categories/>
  <Services/>
  <AboutUs/>
  <Pricing/>
  <ContactUs/>
  <Footer/>
</div>
</div>
</template>

<script>
import ContactUs from './components/ContactUs.vue'
import Pricing from './components/Pricing.vue'
import AboutUs from './components/AboutUs.vue'
import Services from './components/Services.vue'
import Navbar from './components/Navbar.vue'
import Header from './components/Header.vue'
import Categories from './components/Categories.vue'
import Footer from "./components/Footer.vue"
export default {
  name: 'App',
  components: {
    Navbar,
    Header,
    Categories,
    Services,
    AboutUs,
    Pricing,
    ContactUs,
    Footer,
  }
}
</script>

<style>
* {
  box-sizing: border-box;
  padding: 0;
  margin: 0;
  font-family: "Poppins", sans-serif;
}
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  /* text-align: center;
  color: #2c3e50; */
  /* margin-top: 60px; */
}
</style>
