<script setup lang="ts">
  import { ref } from 'vue';

  const isMobile = ref<boolean>(false)

  const handleMenu = () => {
    isMobile.value = !isMobile.value

    console.log(isMobile.value)
  }
</script>

<template>
  <header class="header">
    <span class="header__logo">
      Cega.Fi
    </span>
    <div :class="['header__navigation__container', { 'open': isMobile }]">
      <nav :class="['header__navigation', { 'open': isMobile }]">
        <ul>
          <li>
            <a href="#">Stories</a>
          </li>
          <li>
            <a href="#">Roadmap</a>
          </li>
          <li>
            <a href="#">Tokenomics</a>
          </li>
          <li>
            <a href="#">Community</a>
          </li>
          <li>
            <a href="#">Blog</a>
          </li>
        </ul>
      </nav>
        <a href="#" :class="['header__wallet', { 'open': isMobile }]">
          Connect Wallet
        </a>
    </div>
    <button ref="isOpen" @click="handleMenu" class="header__menu">
      <i class="fas fa-bars" v-if="!isMobile"></i>
      <i class="fas fa-times" v-else></i>
    </button>
</header>
</template>

<style scoped lang="sass">
  @import "../sass/_variables.sass"
  @import '../sass/_mixins.sass'

  @keyframes menu-animation
    from
      left: 100%
    to
      left: 0

  .header
    position: relative
    max-width: 1200px
    margin: 0 auto
    width: 100%
    display: flex
    align-items: center
    justify-content: space-between

    padding: $gap-xl $gap-sm

    &__logo
      font-size: $text-2xl
      font-family: $font-hanken-grotesk
      font-weight: bold

    &__navigation__container
      display: none

      @media (min-width: 768px)
        width: 100%
        display: flex
        align-items: center
        justify-content: space-between

    &__navigation__container.open
      display: flex
      flex-direction: column
      position: absolute
      top: 4rem
      right: 0
      bottom: 0
      left: 0

      animation: menu-animation 1s ease-in

      width: 100%
      height: 100vh

      z-index: 10
      background: $text-white-color

      @media (min-width: 768px)
        position: relative
        flex-direction: row
        height: auto
        padding: 0
        top: 0
        width: 100%

    &__navigation
      max-width: 31.25rem
      width: 100%
      margin: 0 auto
      display: flex
      align-items: center

      ul
        width: 100%
        display: flex
        align-items: center
        justify-content: space-evenly

        li
          font-size: $text-base

        a
          font-family: $font-space-grotesk

          transition: all 0.4s
          color: $text-color

          &:hover
            text-decoration: underline

    &__navigation.open
      padding-top: 4rem

      @media (min-width: 768px)
        padding-top: 0

      ul
        flex-direction: column
        gap: $gap-base

        @media (min-width: 768px)
          flex-direction: row
          


    &__wallet
      font-size: $text-base
      padding: $gap-md

      border-radius: $gap-sm

      transition: all 0.4s
      color: $text-color

      border: 1px solid $background-button-black
      

      &:hover
        opacity: 0.9
        color: $text-white-color
        background: $background-button-black

    &__wallet.open
      width: fit-content
      margin: 0 auto
      margin-top: 3rem

      @media (min-width: 768px)
        margin-top: 0

    &__menu
      background: transparent
      border: none

      @media (min-width: 768px)
          display: none
    i
      font-size: $text-2xl

</style>