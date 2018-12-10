<template lang="pug">
section.app-header
  header
    .primary
      img(src="/images/menu.png")
    .secondary
      .notification
        img(src="/images/notification.png")
        img.email(src="/images/inbox.png")
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

//secondary
.secondary
  @include flex
  .notification
    margin: $space*1.5
    img.email
      width: 2rem
      margin-left: $space
</style>
