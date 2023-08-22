<script setup lang="ts">
  defineProps({
    image: String,
    background: String,
  })
</script>

<template>
  <div class="nft" :style="{ background: background }">
    <img :src="image" alt="Imagem do card" v-if="image" />
  </div>
</template>

<style scoped lang="sass">
  @import "../sass/_variables.sass"

  .nft
    max-width: 400px
    width: 100%
    margin: 0 auto
    
    border: 6px solid $background-button-black
    border-radius: $gap-sm

    padding-top: $gap-sm

    img
      width: 100%
      height: 100%
</style>