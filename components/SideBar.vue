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
  border-right: 1px solid rgba($black, 0.2)
  background: $neutral
  .logo
    height: $header-height - 1
    @include flex
    justify-content: flex-start
    border-bottom: 1px solid rgba($black, 0.2)
    h5
      font-size: 1.5rem


//Navigation
section.side-bar
  width: 5rem
  @include fixed-w
  cursor: pointer
  ul.navigation
    line-height: 1rem
    li
      @include flex
      justify-content: flex-start
      padding: $space $space*1.5
      height: 3rem
      img
        width: 1.5rem
      span
        text-align: center
        margin-left: $space*2
        font-size: 1rem
        font-weight: 600
        cursor: pointer
        color: #72777a
        &:hover
          color: $black

//interaction
h5, span
  display: none

section.side-bar
  &:hover
    width: 20rem
    transition: all .4s ease
    z-index: 2000
    li
      // margin: $space/2
    h5, span
      display: block
</style>
