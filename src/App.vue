<template>
  <div id="app">
    <!--<img src="./assets/logo.png">-->
    <h1>{{myAwesomeTitle}}</h1>
    <p>{{renderTime}}</p>
    <div v-for="video in videos">
      <pixar-player :sources="video.sources" :options="video.options"></pixar-player>
      <br>
    </div>
    <!--<about></about>-->
  </div>
</template>

<script>
  import About from './components/Hello'
  import PixarPlayer from './components/PixarPlayer'
  import videosJSON from './assets/VideosJSON'

  export default {
    name: 'app',
    data() {
      return {
        myAwesomeTitle: 'Here is your player , playa',
        renderTime: new Date().toTimeString(),
        videos: videosJSON
      }
    },
    components: {
      About,
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
