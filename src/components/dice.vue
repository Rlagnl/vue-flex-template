<template>
  <div class="dice-box">
    <template v-for="j in 3">
      <div class="column" v-bind:key="'column' + j">
        <template v-for="i in 2">
          <span class="item" v-bind:key="j + 'item' + i"></span>
        </template>
      </div>
    </template>
  </div>
</template>

<script lang='ts'>
  import vue from 'vue'
  export default class App extends vue{}
</script>

<style scoped>
  .dice-box {
    width: 300px;
    height: 300px;
    background-color: aquamarine;
    display: flex;

    /* wrap */
    flex-wrap: wrap;

    /* column | row */
    /* flex-direction: column; */

    /* center | flex-end | space-between */
    /* justify-content: space-between; */

    /* center | flex-end */
    /* align-items: center; */

    /* space-between */
    align-content: space-between;
  }
  .column {
    flex-basis: 100%;
    display: flex;
    justify-content: space-between;
  }
  .item {
    width: 70px;
    height: 70px;
    margin: 15px;
    background-color: black;
    border-radius: 50%;
  }
  .item:nth-child(2) {
    /* center | flex-end */
    /* align-self: center; */
  }
  .item:nth-child(3) {
    /* align-self: flex-end; */
  }
</style>
