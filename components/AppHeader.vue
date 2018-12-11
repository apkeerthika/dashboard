<template lang="pug">
section.app-header
  header
    .primary
      .notification
        img(src="/images/notification.png")
        span 6
      .email
        img(src="/images/inbox.png")
        span 3
      //- img(src="/images/menu.png")
    .secondary
      my-profile

</template>

<script>
import MyProfile from './MyProfile.vue'

export default {
  components: {
    MyProfile
  }
}
</script>

<style lang="sass" scoped>
@import 'assets/styles/includes'

//layout
section.app-header
  border-bottom: 1px solid $neutral
  header
    @include spread
    height: $header-height - 1
    padding: $space
    .primary
    .secondary

//primary
.primary
  @include flex
  position: relative
  img
    width: 1.5rem
  .notification
    margin: $space*2
  .email
    img
      width: 1.5rem
      margin-left: $space

//primary
.notification, .email
  position: relative
  span
    background-color: #ff3c7e
    border-radius: 50px
    color: #fff
    font-size: 10px
    line-height: 1
    padding: 3px 5px
    @include absolute-ne
    // left: 0.5rem
    right: -0.2rem
    top: -0.2rem

.email
  > span
    top: -0.2rem
</style>
