<template>
<div id="mainPlayer"></div>
</template>

  <script>
     export default {
         data: () => ({
             url: 'http://www.streambox.fr/playlists/x36xhzz/x36xhzz.m3u8',
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
                     parentId: "#mainPlayer",
                     height: 480,
                     width: 854
                 })
                 console.log('Player is loaded')
             }
         }
     }
     </script>

<style scoped>
#mainPlayer {
  text-align: center;
  position: absolute;
  left: 100px;
  border: 1px solid blue;
}
</style>
