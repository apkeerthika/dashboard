<template lang="pug">
section.sale-report
  .container
    .report
      h6 Sales Report
      .total-report
        h3 November 2017
        h5 Sales Report
        span $6000
      .report-table
        table
          thead
            tr
              th Name
              th Status
              th Date
              th Price
          tbody
            tr(v-for="r, i in reports")
              td
                span {{ r.name }}
              td
                span(:class="r.class") {{ r.status }}
              td
                span {{ r.date }}
              td
                span {{ r.price }}

    weather.weather

</template>

<script>
import Weather from './Weather'
export default {
  data () {
    return {
      labels: [
        {
          label: 'Name',
        },
        {
          label: 'Status',
        },
        {
          label: 'Date',
        },
        {
          label: 'Price',
        }
      ],
      reports: [
        {
          name: 'Item #1 Name',
          status: 'Unavailble',
          price: '$12',
          date: 'Nov 18',
          class: 'red'
        },
        {
          name: 'Item #2 Name',
          status: 'New',
          price: '$34',
          date: 'Nov 19',
          class: 'purple'
        },
        {
          name: 'Item #3 Name',
          status: 'New',
          price: '-$45',
          date: 'Nov 20',
          class: 'red'
        },
        {
          name: 'Item #4 Name',
          status: 'Unavailable',
          price: '$65',
          date: 'Nov 21',
          class: 'green'
        },
        {
          name: 'Item #5 Name',
          status: 'Used',
          price: '$78',
          date: 'Nov 22',
          class: 'red'
        },
        {
          name: 'Item #6 Name',
          status: 'Used',
          price: '-$88',
          date: 'Nov 23',
          class: 'red'
        },
        {
          name: 'Item #7 Name',
          status: 'Old',
          price: '$56',
          date: 'Nov 22',
          class: 'yellow'
        },
      ]
    }
  },
  components: {
    Weather
  }
}
</script>

<style lang="sass" scoped>
@import 'assets/styles/includes'

section.sale-report
  padding-top: $space*3
  .container
    @include flex
    align-items: flex-start
    padding-left: $space*9.5
    .report
      width: 50%
    weather.weather
      flex: 1
//total-report
.report
  position: relative
  h6
    color: #72777a
    letter-spacing: 1px
    font-weight: 600
    font-size: 1.2rem
  .total-report
    background-color: $dash-blue
    color: $white
    padding: $space*2
    position: relative
    margin-top: $space*2
    span
      @include absolute-e
      font-weight: bold
      font-size: 2rem
      top: 50%
      right: 2rem

//table
.report-table
  width: 100%
  background: $white
  padding: $space*3
  border-collapse: collapse
  tr
    th
      text-align: left
      border-bottom: 1px solid rgba($black, .0625)
      color: #72777a
      letter-spacing: 1px
      font-weight: 600
      font-size: 1.2rem
      padding: $space/2
  tr
    td
      padding: $space/2
      border-bottom: 1px solid rgba($black, .0625)
      span
        text-align: left
        color: #72777a
        letter-spacing: 1px
        font-weight: 600
        font-size: 1rem


table
  height: 25rem
  width: 100%

td
  span.red
    background: #ffebee
    color: $dash-red !important
    padding: 5px
    font-size: 0.9rem !important
    border-radius: 10px
  span.green
    background: #e8f5e9
    color: $dash-green !important
    padding: 5px
    font-size: 0.9rem !important
    border-radius: 10px
  span.purple
    background: #ede7f6
    color: $dash-purple !important
    padding: 5px
    font-size: 0.9rem !important
    border-radius: 10px
  span.yellow
    background: #fffde7
    color: $dash-yellow !important
    padding: 5px
    font-size: 0.9rem !important
    border-radius: 10px
</style>
