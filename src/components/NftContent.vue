<script setup lang="ts">
  import NftCard from './NftCard.vue'

  import  { ntfCards } from '../utils/nftCards'

</script>

<template>
  <div class="nft__content">
    <h2>Latest Auction</h2>
    <div class="nft__cards">
        <template v-for="card in ntfCards">
            <NftCard :image="card.image" :background="card.background" />
        </template>
    </div>
  </div>
</template>

<style scoped lang="sass">
  @import "../sass/_variables.sass"

  .nft__content
    width: 100%
    display: flex
    flex-direction: column
    gap: $gap-base

    margin-top: 3rem

  h2
    font-family: $font-hanken-grotesk
    font-size: $text-4xl

  .nft__cards
    width: 100%
    display: grid
    gap: 3rem
    grid-template-columns: 1fr

    @media (min-width: 640px)
      grid-template-columns: repeat(2, 1fr)

    @media (min-width: 768px)
      grid-template-columns: repeat(3, 1fr)

    @media (min-width: 1024px)
      grid-template-columns: repeat(4, 1fr)
      justify-content: space-between

</style>