<template lang="pug">
section.dashboard
  aside
    side-bar
  main
    app-header
    total-visit
    location
    monthly-stats
</template>

<script>
import SideBar from './SideBar'
import AppHeader from './AppHeader'
import TotalVisit from './TotalVisit'
import Location from './Location'
import MonthlyStats from './MonthlyStats'

export default {
  components: {
    SideBar,
    AppHeader,
    TotalVisit,
    Location,
    MonthlyStats
  }
}
</script>

<style lang="sass" scoped>
@import 'assets/styles/includes'

section.dashboard
  .container
    @include flex
    align-items: flex-start
    // padding-left: 0
    aside
    main
      flex: 1
</style>
