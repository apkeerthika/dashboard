<template lang="pug">
section.side-bar
  .logo
    img(src="/images/logo.png")
    h5 Adminator
  ul.navigation
    li(v-for="nav, i in items", :key="i")
      img(:src="nav.icon")
      span {{ nav.label }}
</template>

<script>
import navigation from 'static/seed/navigation'

export default {
  data () {
    return {
      items: navigation
    }
  }
}
</script>

<style lang="sass" scoped>
@import 'assets/styles/includes'

section.side-bar
  min-height: 100vh
  border-right: 1px solid $neutral
  .logo
    @include flex
    justify-content: center
    border-bottom: 1px solid $neutral
    padding: $space/2
    h5
      font-size: 1.5rem


//Navigation
section.side-bar
  ul.navigation
    line-height: 1.5rem
    li
      margin: $space*2 $space*4
      display: block
      color: #72777a
      img
        width: 2rem
      span
        text-align: center
        margin-left: $space*2
        font-size: 1.5rem
        cursor: pointer
        &:hover
          color: $black
</style>
