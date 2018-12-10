<template lang="pug">
.my-profile
  img(src="/images/jhon.jpg")
  span John Doe
</template>

<style lang="sass" scoped>
@import 'assets/styles/includes'

.my-profile
  @include flex
  img
    border-radius: 50%
    width: 3rem
  span
    margin-left: $space/2
</style>
