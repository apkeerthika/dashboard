<template lang="pug">
section.app-header
  header
    .primary
      .notification
        img(src="/images/notification.png")
        img.email(src="/images/inbox.png")
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
  img
    width: 2rem
  .notification
    margin: $space*2

//secondary
.secondary
  @include flex
  img.email
    width: 2rem
    margin-left: $space
</style>
