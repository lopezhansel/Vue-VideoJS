<template>
  <div class="pixar-player">
    <h1>{{myAwesomeTitle}}</h1>
    <p>{{renderTime}}</p>
    <video id="my-video" class="video-js" controls preload="auto" width="640" height="264" poster="http://d2zihajmogu5jn.cloudfront.net/tears-of-steel/tears_of_steel.jpg"
      data-setup="{}">
      <!-- THESE IS THE STANDARD OF TELLING THE WAY OF TELLING THE PLAYER THE VIDEO INFO-->
      <source src="http://www.sample-videos.com/video/mp4/720/big_buck_bunny_720p_1mb.mp4" type='video/mp4'>
      <source src="MY_VIDEO.webm" type='video/webm'>
      <p class="vjs-no-js">
        To view this video please enable JavaScript, and consider upgrading to a web browser that
        <a href="http://videojs.com/html5-video-support/" target="_blank">supports HTML5 video</a>
      </p>
    </video>
  </div>
</template>

<script>
  export default {
    name: 'pixar-player',
    data() {
      return {
        myAwesomeTitle: 'Here is your player , playa',
        renderTime: new Date().toTimeString(),
      }
    },
    created() {
      // this runs when component is created
    }
  }

</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
  h1,
  h2 {
    font-weight: normal;
  }
  
  ul {
    list-style-type: none;
    padding: 0;
  }
  
  li {
    display: inline-block;
    margin: 0 10px;
  }
  
  a {
    color: #42b983;
  }

</style>
