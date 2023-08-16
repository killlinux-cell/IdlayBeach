<template>
  <Navbar></Navbar>
  <Hero></Hero>
  <About></About>
  <Gallery></Gallery>
  <Contact></Contact>
  <Footer></Footer>
</template>

<script>
import Navbar from './components/Navbar.vue';
import Hero from './components/Hero.vue';
import About from './components/About.vue';
import Gallery from './components/Gallery.vue';
import Contact from './components/Contact.vue';
import Footer from './components/Footer.vue';


export default{
  name: 'App',

  components:{
    Navbar,
    Hero,
    About,
    Gallery,
    Contact,
    Footer,
  }
}
</script>


<style>
@import './style.css';

</style>
