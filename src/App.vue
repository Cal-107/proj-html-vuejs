<template>
  <div id="app">

    <!-- Start Header -->
    <Header />

    <!-- Start Main -->
    <main>
      <Section1 />
    </main>

    <!-- Start Footer -->
    <Footer />
  </div>
</template>

<script>
import Header from '@/components/Header.vue';
import Section1 from '@/components/Section1.vue';
import Footer from '@/components/Footer.vue';

export default {
  name: 'App',
  components: {
    Header,
    Section1,
    Footer,
  }
}
</script>

<style lang="scss">
@import '@/styles/variables';
@import '@/styles/globals';
</style>