<template>
  <div class="container">
    <div class="row">
      <Cell />
      <Cell />
      <Cell />
      <Cell />
      <Cell />
    </div>
        <div class="row">
      <Cell />
      <Cell />
      <Cell />
      <Cell />
      <Cell />
    </div>    <div class="row">
      <Cell />
      <Cell />
      <Cell />
      <Cell />
      <Cell />
    </div>    <div class="row">
      <Cell />
      <Cell />
      <Cell />
      <Cell />
      <Cell />
    </div>    <div class="row">
      <Cell />
      <Cell />
      <Cell />
      <Cell />
      <Cell />
    </div>
  </div>
  

</template>

<script>
import Cell from "./components/cell"
export default {
  components: {
    Cell
  }
}

</script>

<style>
  .container {
    width: 100%;
    height: 500px;
    display: flex;
    flex-direction: column;
    align-items: center;
    justify-content: center;
  }
  .row {
    display: flex;
  }
</style>