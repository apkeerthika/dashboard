<template lang="pug">
.my-profile
  a(@click="showMenu")
    img(src="/images/jhon.jpg")
    h5 John Doe
  .mask(v-if="open" @click="hideMenu()")
  .popup(v-if="open")
    ul.items-list
      li
        img(src="/images/settings.png")
        nuxt-link#link(to="/") Settings
      li
        img(src="/images/profile.png")
        nuxt-link#link(to="/") Profile
      li
        img(src="/images/message.png")
        nuxt-link#link(to="/") Messages
      li
        img(src="/images/logout.png")
        nuxt-link(to="/") Logout
</template>


<script>
export default {
  data () {
    return {
      open: false
    }
  },
  methods: {
    showMenu () {
      this.open = !this.open
    },
    hideMenu () {
      this.open = false
    }
  }
}
</script>

<style lang="sass" scoped>
@import 'assets/styles/includes'

.my-profile
  position: relative
  transition: transform .15s ease-out,-webkit-transform .15s ease-out
  a
    @include flex
    cursor: pointer
    img
      border-radius: 50%
      width: 3rem
    h5
      margin-left: $space/2

//mask
.mask
  @include fixed
.popup
  @include absolute
  top: 140%
  right: 0
  left: auto
  ul.items-list
    width: 15rem
    padding: $space 0
    background-color: #fff
    border: 1px solid rgba(0,0,0,.15)
    border-radius: .25rem
    li
      @include stack-l
      padding: $space $space/2
      img
        width: 1.5rem
      a
        color: $black
        margin-left: $space
      &:last-child
        border-top: 1px solid $neutral
      &:hover
        background: $neutral
</style>
