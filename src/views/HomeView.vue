<template>
  <div class="home">
    <Navbar />
    <Main />
    <Footer />
  </div>
</template>

<script>
import Footer from '@/components/Footer/Footer.vue';
import Main from '@/components/Main/Main.vue';
import Navbar from '@/components/Navbar.vue';

export default {
  name: 'HomeView',
  components: {
    Navbar,
    Main,
    Footer
  }
}
</script>
