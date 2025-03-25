<template>
  <div id="app">
    <Navbar />
    <Header />
    <Teaser />
    <Review />
  </div>
</template>

<script>
import Navbar from './components/Navbar.vue'
import Header from './components/Header.vue'
import Teaser from './components/teaser.vue';
import Review from './components/Review.vue';

export default {
  name: 'App',
  components: {
    Navbar,
    Header,
    Teaser,
    Review
  },
}
</script>
