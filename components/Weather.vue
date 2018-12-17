<template lang="pug">
section.weather
  .container
    h6 Weather
  //- weather(
  //-   api-key="<your-dark-sky-api-key>"
  //-   title="Weather"
  //-   latitude="24.886436"
  //-   longitude="91.880722"
  //-   language="en"
  //-   units="uk")
</template>

<script>
// import VueWeatherWidget from 'vue-weather-widget'
// import 'vue-weather-widget/dist/css/vue-weather-widget.css'

export default {
  components: {
    // 'weather': VueWeatherWidget
  }
}
</script>

<style lang="sass" scoped>
@import 'assets/styles/includes'

section.weather
  .container
    padding-left: 0 !important

h6
  color: #72777a
  letter-spacing: 1px
  font-weight: 600
  font-size: 1.2rem
</style>
