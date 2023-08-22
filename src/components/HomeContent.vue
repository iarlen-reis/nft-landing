<script setup lang="ts">
  import HomeImage from '../assets/homeImage.png'
</script>

<template>
  <div class="home">
    <div class="home__apresentation">
      <div class="home__introduction">
        <span>Best Opensea Newcomer 🔥</span>
        <h1>Cega Super Sanics</h1>
      </div>
      <div class="home__details">
        <p>
          Cega’s Super Sanics are 10,000 unique & high utility NFTs for the Cega DeFi 
          exotic options protocol. We combine the best of defi with the best of NFTs.
        </p>
        <div class="home__details__buttons">
          <button>Join wishlist <span></span></button>
          <button>Learn more <span></span></button>
        </div>
      </div>
    </div>
    <div class="home__image">
      <img :src="HomeImage" alt="imagem do super sanics">
    </div>
  </div>
</template>

<style lang="sass" scoped>
  @import "../sass/_variables.sass"

  .home
    display: grid
    grid-template-columns: 1fr

    margin: 0 auto

    @media (min-width: 768px)
      margin-top: 3rem

    @media (min-width: 1024px)
      width: 100%
      align-items: center
      grid-template-columns: 1fr 1fr
      gap: $gap-xl
      
      justify-content: space-between

    &__apresentation
      display: flex
      flex-direction: column
      gap: $gap-md

      @media (min-width: 768px)
        gap: $gap-xl

    &__introduction
      display: flex
      flex-direction: column
      gap: $gap-xs

      span
        width: fit-content
        font-family: $font-space-grotesk
        font-size: $text-base

        padding: $gap-sm $gap-base

        border-radius: $gap-base

        color: $text-white-color
        background: $background-button-black


      h1 
        font-size: $text-4xl

        @media (min-width: 768px)
          font-family: $font-hanken-grotesk
          font-size: $text-5xl
          font-weight: bold


    &__details
      display: flex
      flex-direction: column
      gap: $gap-xl

      p
        max-width: 39.375rem
        font-family: $font-space-grotesk
        font-size: $text-base

        @media (min-width: 768px)
          font-size: $text-xl

    &__details__buttons
      width: 100%
      display: flex
      gap: $gap-xl

      margin-top: 0.5rem

      button
        position: relative
        font-family: $font-space-grotesk
        font-size: $text-xl

        padding: $text-sm 1.4rem

        border: none
        cursor: pointer

        transition: all 0.4s
        color: $text-white-color

        @media (min-width: 680px)
          padding: $text-xl 2.3rem


        @media (min-width: 768px)
          padding: $text-xl 2.8rem


        &:nth-child(1)
          background: $background-button

          &:hover
            background: rgb(100, 0, 255)

          span
            background: $background-button-black

        &:nth-child(2)
          background: $background-button-black

          &:hover
            background: rgb(9, 0, 40)

          span
            background: $background-button
          

        span
          position: absolute
          width: 7rem
          height: 100%

          left: 0
          right: 0
          top: -$gap-sm

          z-index: -1

          margin: 0 auto

          @media (min-width: 680px)
            width: 8.5rem

          @media (min-width: 768px)
            width: 10.6rem


    &__image
      width: 100%
      max-width: 22rem
      margin: 0 auto
      margin-top: 3rem

      @media (min-width: 640px)
        max-width: 32rem

      @media (min-width: 1024px)
        margin-top: 3rem
        max-width: 38rem
        width: 100%

      img
        width: 100%

</style>