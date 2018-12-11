<template lang="pug">
section.dashboard
  .container
    aside
      side-bar
    main
      app-header
      total-visit
</template>

<script>
import SideBar from './SideBar'
import AppHeader from './AppHeader'
import TotalVisit from './TotalVisit'

export default {
  components: {
    SideBar,
    AppHeader,
    TotalVisit
  }
}
</script>

<style lang="sass" scoped>
@import 'assets/styles/includes'

section.dashboard
  .container
    @include flex
    align-items: flex-start
    padding-left: 0
    aside
      background: $white
    main
      flex: 1
</style>
