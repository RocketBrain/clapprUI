<template>
  <div id="app">
    <mainPlayer></mainPlayer>
    <sidePlayer></sidePlayer>
    <thumb2></thumb2>
    <thumb3></thumb3>
    <thumb4></thumb4>

  </div>
</template>

<script>
import mainPlayer from './components/mainPlayer.vue'
import sidePlayer from './components/sidePlayer.vue'
import thumb2 from './components/thumb2.vue'
import thumb3 from './components/thumb3.vue'
import thumb4 from './components/thumb4.vue'



export default {
  name: 'app',
  components: {
    'mainPlayer': mainPlayer,
    'sidePlayer': sidePlayer,
    'thumb2' : thumb2,
    'thumb3' : thumb3,
    'thumb4' : thumb4

  }
}
</script>


<style scoped>
#app {
  position: relative;
  width: 1600px;
  margin-top: 5%;
  left: 50px;
}
</style>
