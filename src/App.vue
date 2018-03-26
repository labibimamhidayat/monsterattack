<template>
  <div id="app">
    <el-container>
      <el-main>
        <atm-wrap>
          <atm-title>
            Attack On The Monster
          </atm-title>
          <el-row gutter="40">
            <atm-lifebar :percentage="playerLife" :label="'player'"></atm-lifebar>
            <atm-lifebar :percentage="monsterLife" :label="'monster'"></atm-lifebar>
          </el-row>
        </atm-wrap>
      </el-main>
    </el-container>
  </div>
</template>

<script>
import wrapper from './components/wrapper'
import header from './components/header'
import lifebar from './components/lifebar'
export default {
  name: 'App',
  components: {
    'atm-wrap' : wrapper,
    'atm-title' : header,
    'atm-lifebar' : lifebar
  },
  data(){
    return {
      playerLife : 100,
      monsterLife : 50
    }
  },
  methods: {
    minLifePlayer(){  
      this.playerLife  = this.playerLife - 1
    }
  }
}
</script>

<style scoped>
  #app {
    font-family: 'Avenir', Helvetica, Arial, sans-serif;
    -webkit-font-smoothing: antialiased;
    -moz-osx-font-smoothing: grayscale;
    padding-top: 50px;
    padding-bottom: 50px;
  }
</style>
