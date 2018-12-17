<template lang="pug">
section.monthly-stats
  .container
    .stats
      img(src="https://cdn-images-1.medium.com/max/1600/1*3L_OB5rwF7af1EpvR5kQIQ.png")
    todo-list.list
</template>

<script>
import TodoList from './TodoList'

export default {
  components: {
    TodoList
  }
}
</script>

<style lang="sass" scoped>
@import 'assets/styles/includes'

section.monthly-stats
  padding-top: $space*2
  .container
    @include flex
    padding-left: $space*9.5
    .stats, .list
      width: 50%
      background: $white
      // margin: $space/2 $space 0 0
    .list
      margin: 0 $space
      border: 1px solid rgba($black, .0625)

.stats
  img
    width: 100%
    height: 80%
</style>
