<template>
  <div class="container">
    <h1>{{step}}</h1>
    <div class="row">
      <Cell v-on:stepAdd="stepAdd" v-bind:step="step" />
      <Cell v-on:stepAdd="stepAdd" v-bind:step="step" />
      <Cell v-on:stepAdd="stepAdd" v-bind:step="step" />
      <Cell v-on:stepAdd="stepAdd" v-bind:step="step" />
      <Cell v-on:stepAdd="stepAdd" v-bind:step="step" />
    </div>
    <div class="row">
      <Cell v-on:stepAdd="stepAdd" v-bind:step="step" />
      <Cell v-on:stepAdd="stepAdd" v-bind:step="step" />
      <Cell v-on:stepAdd="stepAdd" v-bind:step="step" />
      <Cell v-on:stepAdd="stepAdd" v-bind:step="step" />
      <Cell v-on:stepAdd="stepAdd" v-bind:step="step" />
    </div>    <div class="row">
      <Cell v-on:stepAdd="stepAdd" v-bind:step="step" />
      <Cell v-on:stepAdd="stepAdd" v-bind:step="step" />
      <Cell v-on:stepAdd="stepAdd" v-bind:step="step" />
      <Cell v-on:stepAdd="stepAdd" v-bind:step="step" />
      <Cell v-on:stepAdd="stepAdd" v-bind:step="step" />
    </div>    <div class="row">
      <Cell v-on:stepAdd="stepAdd" v-bind:step="step" />
      <Cell v-on:stepAdd="stepAdd" v-bind:step="step" />
      <Cell v-on:stepAdd="stepAdd" v-bind:step="step" />
      <Cell v-on:stepAdd="stepAdd" v-bind:step="step" />
      <Cell v-on:stepAdd="stepAdd" v-bind:step="step" />
    </div>    <div class="row">
      <Cell v-on:stepAdd="stepAdd" v-bind:step="step" />
      <Cell v-on:stepAdd="stepAdd" v-bind:step="step" />
      <Cell v-on:stepAdd="stepAdd" v-bind:step="step" />
      <Cell v-on:stepAdd="stepAdd" v-bind:step="step" />
      <Cell v-on:stepAdd="stepAdd" v-bind:step="step" />
    </div>
  </div>
  

</template>

<script>
import Cell from "./components/cell"
export default {
  components: {
    Cell
  },
  data() {
    return {
      step:0,
      map: []
    }
  },
  methods: {
    stepAdd() {
      this.step++
    }
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