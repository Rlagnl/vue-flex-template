<template>
  <div class="gridding-box">
    <div class="Grid-cell u-1of4">...</div>
    <div class="Grid-cell">...</div>
    <div class="Grid-cell u-1of3">...</div>
  </div>
</template>

<script lang='ts'>
  import vue from 'vue'
  export default class App extends vue{}
</script>

<style scoped>
  .gridding-box {
    width: 300px;
    height: 300px;
    background-color: aquamarine;
    display: flex;
  }

  .Grid-cell {
    flex: 1;
  }

  .Grid-cell.u-full {
    flex: 0 0 100%;
    background-color: red;
  }

  .Grid-cell.u-1of2 {
    flex: 0 0 50%;
    background-color: blue;
  }

  .Grid-cell.u-1of3 {
    flex: 0 0 33.3333%;
    background-color: green;
  }

  .Grid-cell.u-1of4 {
    flex: 0 0 25%;
    background-color: yellow;
  }
</style>
