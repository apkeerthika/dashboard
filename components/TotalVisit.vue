<template lang="pug">
section.total-visit
  .visits(v-for="v, i in visits", :key="i")
    .visit
      .visit-name
        h6 {{ v.label }}
      .visit-percentage
        img(:src="v.image")
        span(:class="v.class") {{ v.percentage }}

</template>

<script>
export default {
  data () {
    return {
      visits: [
        {
          label: 'Total Visits',
          image: '/images/visit.png',
          percentage: '+10%',
          class: 'green'
        },
        {
          label: 'Total Page Views',
          image: '/images/view.png',
          percentage: '-7%',
          class: 'purple'
        },
        {
          label: 'Unique Visitor',
          image: '/images/visitor.png',
          percentage: '~12%',
          class: 'blue'
        },
        {
          label: 'Bounce Rate',
          image: '/images/rate.png',
          percentage: '33%',
          class: 'red'
        },
      ]
    }
  }
}
</script>


<style lang="sass" scoped>
@import 'assets/styles/includes'

section.total-visit
  @include flex
  background: $white
  padding: $space
  .visits
    border: 1px solid rgba($black, 0.1)
    width: 25%
    margin: $space
    .visit
      padding: $space


//rate
.visit-percentage
  @include flex
  margin-top: $space*3
  img
    width: 2rem


//name
.visit-name
  h6
    color: #72777a
    letter-spacing: 1px
    font-weight: 600
    font-size: 1.2rem


//percentage
span.green
  background-color: #e8f5e9 !important
  padding: $space/2 $space
  border-radius: 2rem
  font-weight: bold
  font-size: 1rem
  color: $dash-green
span.purple
  background-color: #ffebee !important
  padding: $space/2 $space
  border-radius: 2rem
  font-weight: bold
  font-size: 1rem
  color: $dash-red
span.blue
  background-color: #f3e5f5 !important
  padding: $space/2 $space
  border-radius: 2rem
  font-weight: bold
  font-size: 1rem
  color: $dash-purple
span.red
  background-color: #e3f2fd !important
  padding: $space/2 $space
  border-radius: 2rem
  font-weight: bold
  font-size: 1rem
  color: $dash-blue
</style>
