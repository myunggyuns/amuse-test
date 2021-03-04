<template>
  <div id="app">
    <photo-view msg="Welcome Photo book" :images="images" />
  </div>
</template>

<script>
import PhotoView from './components/PhotoView.vue';
import photodata from "./assets/photodata";

export default {
  name: 'App',
  data() {
    return {
      images: photodata,
    }
  },
  components: {
    PhotoView
  }
}
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
}
</style>
