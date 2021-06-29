<template>
  <div id="app">
      <SocNet :array="messageArray" />
  </div>
</template>

<script>
import SocNet from './components/SocNet'

export default {
  name: 'App',
  components: {
    SocNet
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
