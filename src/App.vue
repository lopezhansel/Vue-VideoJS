<template>
  <div id="app">
    <!--<img src="./assets/logo.png">-->
    <pixar-player :sources="video.sources" :options="video.options"></pixar-player>
    <!--<hello></hello>-->
  </div>
</template>

<script>
  import Hello from './components/Hello'
  import PixarPlayer from './components/PixarPlayer'

  export default {
    name: 'app',
    data () {
      return {
          video: {
            sources: [
              {
                // src: 'http://covteam.u.qiniudn.com/oceans.mp4',
                src: 'http://www.sample-videos.com/video/mp4/720/big_buck_bunny_720p_1mb.mp4',
                type: 'video/mp4'
              }
            ],
            options: {
              autoplay: true,
              volume: 0.6,
              // poster: 'http://d2zihajmogu5jn.cloudfront.net/tears-of-steel/tears_of_steel.jpg'
              poster: 'http://covteam.u.qiniudn.com/poster.png'
            }
          }
        }  
      },
    components: {
      Hello,
      PixarPlayer 
    }
  }

</script>

<style>
  #app {
    font-family: 'Avenir', Helvetica, Arial, sans-serif;
    -webkit-font-smoothing: antialiased;
    -moz-osx-font-smoothing: grayscale;
    text-align: center;
    color: #2c3e50;
    margin-top: 60px;
  }

</style>

