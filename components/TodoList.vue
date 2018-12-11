<template lang="pug">
.todo-list
  h6 Todo List
  ul.lists
    li.list(v-for="l, i in lists", :key="i")
      input(type="checkbox")
      label {{ l.label }}
      span(:class="l.class") {{ l.time }}
</template>

<script>
export default {
  data () {
    return {
      lists: [
        {
          label: 'Call Jhon for Dinner',
        },
        {
          label: 'Book Boss Flight',
          time: '2 Days',
          class: 'green'
        },
        {
          label: 'Hit the Gym',
          time: '3 Minutes',
          class: 'red'
        },
        {
          label: 'give Purchase Report',
          time: 'not important',
          class: 'yellow'
        },
        {
          label: 'Watch Game o Thrones Episode',
          time: 'Tomorrow',
          class: 'teal'
        },
        {
          label: 'Give Purchase report',
          time: 'Done',
          class: 'green'
        },
      ]
    }
  }
}
</script>



<style lang="sass" scoped>
@import 'assets/styles/includes'

.todo-list
  padding: $space*2
  h6
    color: #72777a
    letter-spacing: 1px
    font-weight: 600
    font-size: 1.2rem


//input
ul.lists
  position: relative
  li.list
    margin: $space*2.5
    position: relative
    label
      margin-left: $space
      color: #72777a
      letter-spacing: 1px
      font-weight: normal
      font-size: 1.2rem
    span
      @include absolute-e
      text-align: center

//color
span.green
  background: $dash-green
  color: $white
  font-weight: bold
  height: 2rem
  border-radius: 20px
  padding: $space/2 $space
span.red
  background: $dash-red
  color: $white
  font-weight: bold
  height: 2rem
  border-radius: 20px
  padding: $space/2 $space
span.yellow
  background: #ffeb3b
  color: $black
  font-weight: bold
  height: 2rem
  border-radius: 20px
  padding: $space/2 $space
span.teal
  background: #00bcd4
  color: $white
  font-weight: bold
  height: 2rem
  border-radius: 20px
  padding: $space/2 $space
</style>
