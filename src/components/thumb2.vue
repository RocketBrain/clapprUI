<template>
<div id="thumb2"></div>
</template>

  <script>
     export default {
         data: () => ({
             url: 'https://bitdash-a.akamaihd.net/content/MI201109210084_1/m3u8s/f08e80da-bf1d-4e3d-8899-f0f6155f6efa.m3u8',
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
                     parentId: "#thumb2",
                     height: 120,
                     width: 220
                 })
                 console.log('Player is loaded')
             },

         }
     }
     </script>

<style scoped>
#thumb2 {
  width: 220px;
  text-align: center;
  position: absolute;
  right: 25%;
  border: 1px solid blue;
  top: 150px;
}
</style>
