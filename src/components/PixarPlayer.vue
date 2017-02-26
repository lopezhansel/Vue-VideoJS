<template>
  <div class="pixar-player">
    <link href="http://vjs.zencdn.net/5.16.0/video-js.css" rel="stylesheet">
    <div class="pixar-controls">
      <button type="text" @click="onPlay()">Play</button>
      <button type="text" @click="onPause()">Pause</button>
    </div>
    <video id="my-video" class="video-js" controls preload="auto" width="640" height="264" :poster="options.poster" data-setup="{}">
      <source v-for="source in sources" :src="source.src" :type="source.type">
      </source>
      <source src="MY_VIDEO.webm" type='video/webm'>
      <p class="vjs-no-js">
        To view this video please enable JavaScript, and consider upgrading to a web browser that
        <a href="http://videojs.com/html5-video-support/" target="_blank">supports HTML5 video</a>
      </p>
    </video>
  </div>
</template>

<script>
  import videojs from 'video.js'
  export default {
    name: 'pixar-player',
    props: {
      sources: Array,
      options: {
        type: Object,
        default () {
          return {
            autoplay: false,
            volume: 0.9,
            poster: ''
          }
        }
      }
    },
    data() {
      return {
        $video: null,
        onPlay() {
          this.$video.play()
        },
        onPause() {
          this.$video.pause()
        }
      }
    },
    mounted() {
      this.$video = videojs(this.$el.getElementsByTagName('video')[0])
      console.info(this.$video)
    },
    created() {}
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
