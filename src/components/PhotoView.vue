<template>
  <div class="root" v-on:click.self="do_X">
    <h1 v-on:click.self="do_X">{{ msg }}</h1>
    <gallery class="gallery" :images="images" :index="index" @close="index = null"></gallery>
    <div class="list-box" v-on:click.self="do_X">
      <div
        class="image-box"
        v-for="(image, imageIndex) in images"
        :key="imageIndex"
        @click="index = imageIndex"
      >
        <img class="image" :src="`${image}`" alt="" />
      </div>
    </div>
    <template>
    <div class="text-center">
      <v-snackbar
        v-model="snackbar"
        :timeout="timeout"
      >
        {{ text }}
      </v-snackbar>
    </div>
  </template>
  </div>
</template>

<script>
import VueGallery from "vue-gallery";

export default {
  name: 'HelloWorld',
  components: {
    'gallery': VueGallery
  },
  props: {
    msg: String,
    images: Array,
  },
  data: () => ({
    snackbar: false,
    text: 'Click to Image',
    timeout: 1000,
    index: null
  }),
  methods: {
    do_X () {
      this.snackbar= true
      console.log('prevent bubble')
    },
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
h3 {
  margin: 40px 0 0;
}

.root {
  height: 100vh;
}

.list-box {
  display: flex;
  justify-content: center;
  align-items: center;
  flex-wrap: wrap;
  flex: 1;
  width: 100%;
  min-width: 320px;
}

.image-box {
  margin: 5px;
  width: 30%;
  height: 200px;
  cursor: pointer;
}

.image {
  width: 100%;
  height: 100%;
}

</style>
