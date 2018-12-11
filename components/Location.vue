<template lang="pug">
section.location
  .container
    .locationar
      .map
        h6 Site visits
        img(src="https://media.istockphoto.com/photos/world-map-picture-id541303210?k=6&m=541303210&s=612x612&w=0&h=xVNsz2cyBmD7Fsy6aZuyEihHN_sZx21km6abodKHG3s=")
      .progress
        ul
          li(v-for="v, i in visitors", :key="i")
            h6 {{ v.label }}
            .where
              h6.where {{ v.where }}
              span {{ v.howMuch }}
            .line
              .progress-inner(:class="v.class")

        ul.users
          li.user(v-for="u, i in users", :key="i")
            .howMuch
              span {{ u.howMuch }}
            h6 {{ u.label }}
</template>


<script>
export default {
  data () {
    return {
      visitors: [
        {
          label: '100k',
          where: 'Visitors From USA',
          howMuch: '50%',
          class: 'purple'
        },
        {
          label: '1M',
          where: 'Visitors From Europe',
          howMuch: '80%',
          class: 'green'
        },
        {
          label: '450k',
          where: 'Visitors From Australia',
          howMuch: '40%',
          class: 'skyblue'
        },
        {
          label: '1B',
          where: 'Visitors From India',
          howMuch: '90%',
          class: 'darkgreen'
        },
      ],
      users: [
        {
          howMuch: '75%',
          label: 'New users',
        },
        {
          howMuch: '50%',
          label: 'New Purchases',
        },
        {
          howMuch: '90%',
          label: 'Bounce Rate',
        },
      ]
    }
  }
}
</script>

<style lang="sass" scoped>
@import 'assets/styles/includes'


//container
section.location
  padding-top: $space*2
  .container
    min-height: 50vh
    padding-left: $space*9.5
section.location
  .locationar
    @include flex
    align-items: flex-start
    border: 1px solid rgba($black, .0625)
    background: $white
    .map
      width: 60%
      padding: $space
      img
        width: 60%
        height: 100%
        text-align: center
        margin: 0 auto
      h6
        // text-align: center
    .progress
      background: $white
      width: 40%
      padding: $space
      border-bottom: 1px solid rgba($black, .0625)
      border-left: 1px solid rgba($black, .0625)

h6
  color: #72777a
  letter-spacing: 1px
  font-weight: 600
  font-size: 1.2rem

//where
.where
  @include flex
  line-height: 3rem
  h6
    font-size: 0.9rem

//line
.line
  background-color: #eaeef3
  border-radius: 4px
  margin-bottom: 10px
  height: 4px
  width: 100%
  .progress-inner
    background-color: $dash-purple
    width: 50%
    height: 100%
    &.green
      background-color: $dash-green
      width: 80%
    &.skyblue
      background-color: $dash-blue
      width: 40%
    &.darkgreen
      background-color: #607d8b
      width: 90%



//users
ul.users
  @include flex
  margin-top: $space*5
  margin-bottom: $space*3
  li.user
    .howMuch
      border: 2px solid rgba($black, .0625)
      border-radius: 50%
      width: 6rem
      height: 6rem
      position: relative
      span
        text-align: center
        @include absolute
        top: 35%

</style>
