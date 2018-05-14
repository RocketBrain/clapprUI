<template>
<div id="vplayer"></div>
</template>

  <script>
     export default {
         data: () => ({
             url: 'https://bitdash-a.akamaihd.net/content/sintel/hls/playlist.m3u8',
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
                     parentId: "#vplayer",
                     height: 120,
                     width: 220
                 })
                 console.log('Player is loaded')
             },

         }
     }
     </script>

<style scoped>
#vplayer {
  width: 220px;
  text-align: center;
  position: absolute;
  right: 25%;
  border: 1px solid blue;
}
</style>
