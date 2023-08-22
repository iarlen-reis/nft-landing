<script setup lang="ts"></script>

<template>
  <footer class="footer">
      <a href="https://www.figma.com/file/nVvahg1J3LH0cMEYnioLoc/Minimal-NFT-Landing-Page-(Community)?type=design&node-id=21-2&mode=design&t=wxUulYqsddd50pXn-0">&copy; 2023 Cega</a>
  </footer>
</template>

<style scoped lang="sass">
  @import "../sass/_variables.sass"
  .footer
    width: 100%
    max-width: 1200px
    display: flex
    align-items: center
    justify-content: end
    margin: 0 auto
    padding: 2rem $gap-sm

    a
      font-family: $font-space-grotesk
      font-size: $text-base

      color: $text-color

      @media (min-width: 768px)
        font-size: $text-xl

      &:hover
        text-decoration: underline



</style>