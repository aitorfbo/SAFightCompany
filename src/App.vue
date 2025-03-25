<template>
  <div id="app">
    <Navbar />
    <Header />
    <Teaser />
    <Penultimo />
    <Review />
    <Footer />
  </div>
</template>

<script>
import Navbar from './components/Navbar.vue'
import Header from './components/Header.vue'
import Teaser from './components/Teaser.vue';
import Review from './components/Review.vue';
import Footer from './components/Footer.vue';
import Penultimo from './components/Penultimo.vue';

export default {
  name: 'App',
  components: {
    Navbar,
    Header,
    Teaser,
    Review,
    Penultimo,
    Footer
  },
}
</script>
