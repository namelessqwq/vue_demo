<template>
  <div class="container">
    <h2>井字棋</h2>
    <div class="row">
      <Cell v-on:stepAdd="stepAdd(0,$event)" v-bind:step="step" />
      <Cell v-on:stepAdd="stepAdd(1,$event)" v-bind:step="step" />
      <Cell v-on:stepAdd="stepAdd(2,$event)" v-bind:step="step" />
    </div>
    <div class="row">
      <Cell v-on:stepAdd="stepAdd(3,$event)" v-bind:step="step" />
      <Cell v-on:stepAdd="stepAdd(4,$event)" v-bind:step="step" />
      <Cell v-on:stepAdd="stepAdd(5,$event)" v-bind:step="step" />
    </div>    <div class="row">
      <Cell v-on:stepAdd="stepAdd(6,$event)" v-bind:step="step" />
      <Cell v-on:stepAdd="stepAdd(7,$event)" v-bind:step="step" />
      <Cell v-on:stepAdd="stepAdd(8,$event)" v-bind:step="step" />
    </div>
    <div id="result">{{result}}</div>
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
      map: [["null","null","null"],["null","null","null"],["null","null","null"]],
      result: ""
    }
  },
  methods: {
    // 落子
    stepAdd(num,player) {
      this.map[Math.floor(num / 3)][num % 3] = player
      this.step++
      this.tell()
    },
    //胜利判断
    tell() {
      const map = this.map
      //横排判断
      for(let i = 0; i<3 ; i++) {
            console.log(i)
        if(
            map[i][0] != "null" &&
            map[i][0] == map[i][1] &&
            map[i][0] == map[i][2]
          ) {
            if(map[i][0] == 0){
              this.result = "黑子胜利，游戏结束"
            } else {
              this.result = "白子胜利，游戏结束"
            }
        }
      }
      //竖排判断
      for(let i = 0; i<3 ; i++) {
            console.log(i)
        if(
            map[0][i] != "null" &&
            map[0][i] == map[1][i] &&
            map[0][i] == map[2][i]
          ) {
            if(map[0][i] == 0){
              this.result = "黑子胜利，游戏结束"
            } else {
              this.result = "白子胜利，游戏结束"
            }
        }
      }
      //斜线判断
        if((
          map[1][1] != "null" &&
          map[0][0] == map[1][1] &&
          map[0][0] == map[2][2]
      ) || (
          map[1][1] != "null" &&
          map[0][2] == map[1][1] &&
          map[0][2] == map[2][0]
      )
      ) {
        if(map[1][1] == 0){
            this.result = "黑子胜利，游戏结束"
          } else {
            this.result = "白子胜利，游戏结束"
          }
        }
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