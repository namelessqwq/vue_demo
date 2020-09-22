<template>
  <div class="cell" v-on:click="playerClick">
    <div class="black" v-if="player%2 == 0"></div>
    <div class="white" v-if="player%2 == 1"></div>
  </div>
</template>

<script>
  export default {
    data() {
      return {
        player: 0
      }
    },
    methods: {
      playerClick (){
        this.player++
        console.log(this.player)
      }
    }
  }

</script>

<style>
  .cell {
    width: 50px;
    height: 50px;
    border: 1px solid #000;
    display: flex;
    justify-content: center;
    align-items: center;
    margin-top: -1px;
    margin-right: -1px;
  }

  .black,.white {
    width: 35px;
    height: 35px;
    background-color: #fff;
    border: 1px solid #000;
    border-radius: 50%;
    /* display: none; */
  }

  .black {
    background-color: #000;
  }
</style>
