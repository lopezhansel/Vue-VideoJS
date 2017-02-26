<template>
  <div class="pixar-player">
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
      return {}
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
