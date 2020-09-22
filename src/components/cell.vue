<template>
  <div class="cell" v-on:click="playerClick">
    <div v-if="display">
          <div class="black" v-if="text%2 == 0"></div>
          <div class="white" v-if="text%2 == 1"></div>
    </div>
  </div>
</template>

<script>
  export default {
    props: ['step'],
    data() {
      return {
        display: false,
        text: "init"
      }
    },
    methods: {
      playerClick (){
        if(this.text == "init") {
          this.text = this.step
          this.$emit('stepAdd')
        }
        
        if(this.display == false) this.display = !this.display
      }
    },
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
