<template>
  <div id="app">
      <SocNet :array="messageArray" 
      @push="push1"/>

   <game-number/>

  </div>
</template>

<script>
import SocNet from './components/SocialNetwork/SocNet.vue'
import GameNumber from './components/Game/GameNumber.vue'

export default {
  name: 'App',
  components: {
    SocNet,
    GameNumber
  },
  data() {
    return {
      messageArray: [

      ]
    }
  },
  methods: {
    push1(data){
      this.messageArray.push(data)
    }
  }
}
</script>







<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
