<template lang="pug">
.page
  dash-board
</template>


<script>
import DashBoard from '~/components/DashBoard.vue'

export default {
  components: {
    DashBoard
  }
}
</script>

<style lang="sass" scoped>
@import 'assets/styles/includes'

.page
  background: $neutral
</style>

