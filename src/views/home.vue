<template>
  <div class="home-wrapper">
    <!-- <dice /> -->
    <gridding />
  </div>
</template>

<script lang='ts'>
  import vue from 'vue'
  import Component from 'vue-class-component'
  // import Dice from '../components/dice.vue'
  import Gridding from '../components/gridding.vue'

  @Component ({
    components: {
      // Dice,
      Gridding
    }
  })
  export default class App extends vue{}
</script>

<style scoped>

</style>
