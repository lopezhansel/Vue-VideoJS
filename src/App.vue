<template>
  <div id="app">
    <!--<img src="./assets/logo.png">-->
    <h1>Pixar</h1>
    <pixar-player></pixar-player>
    <hello></hello>
  </div>
</template>

<script>
  import Hello from './components/Hello'
  import pixarPlayer from './components/PixarPlayer'

  export default {
    name: 'app',
    components: {
      Hello,
      pixarPlayer 
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

