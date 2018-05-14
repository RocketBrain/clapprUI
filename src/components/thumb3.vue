<template>
<div id="thumb3"></div>
</template>

  <script>
     export default {
         data: () => ({
             url: 'https://mnmedias.api.telequebec.tv/m3u8/29880.m3u8',
             player: null
         }),
         created() {
             let clapprScript = document.createElement('script')
             clapprScript.setAttribute('src', 'https://cdn.jsdelivr.net/npm/clappr@latest/dist/clappr.min.js')
             clapprScript.onload = this.initPlayer;
             document.head.appendChild(clapprScript)
         },
         methods: {
             initPlayer() {
                 this.player = new Clappr.Player({
                     source: this.url,
                     parentId: "#thumb3",
                     height: 120,
                     width: 220
                 })
                 console.log('Player is loaded')
             },

         }
     }
     </script>

<style scoped>
#thumb3 {
  width: 220px;
  text-align: center;
  position: absolute;
  right: 25%;
  border: 1px solid blue;
  top: 300px;
}
</style>
