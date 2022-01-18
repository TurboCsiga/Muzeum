<template>
  <div id="app">
    <button v-on:click="isHidden = !isHidden">Painting</button>
    <button v-on:click="isHidden2 = !isHidden2, isHidden = !isHidden">Mindkettő</button>
    <button v-on:click="isHidden2 = !isHidden2">Statues</button>

    <Painting v-if="!isHidden"></Painting>
    <Statue v-if="!isHidden2"></Statue>
  </div>
</template>



<script>
import Painting from './components/Painting.vue';
import Statue from "./components/Statue.vue";

export default {
  name: 'App',
  
  components: {
    Painting,
    Statue
  },
  data () {
        return {
            isHidden: false,
            isHidden2: false
        }
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
  margin-top: 60px;
}
</style>
