<script setup lang="ts">
  import Header from './components/Header.vue';
  import Footer from './components/Footer.vue';
  import HomeContent from './components/HomeContent.vue';
  import NftContent from './components/NftContent.vue';
  
</script>

<template>
  <Header />
  <main class="main">
    <HomeContent />
    <NftContent />
  </main>
  <Footer />
</template>

<style lang="sass" scoped>
  @import "./sass/_variables.sass"
  
  .main
    max-width: 1200px
    width: 100%
    min-height: 100vh

    display: flex
    flex-direction: column
    gap: $gap-xl
    padding: 0 $gap-sm
    padding-bottom: 4rem

    margin: 0 auto
</style>
