<template>
  <div id="app">
    <!-- <img alt="Vue logo" src="./assets/logo.png"> -->
    <Map msg="Welcome to Your Vue.js App"/>
  </div>
</template>

<script>
import Map from "./components/Map.vue";

export default {
  name: "app",
  components: {
    Map
  }
};
</script>

<style>

body{
  margin: 0;
}
#app {
  position: absolute;
  width: 100%;
  height: 100%;
  margin: 0;
}

#map {
  height: 100%;
  width: 100%;
  margin: 0;
  position: absolute;
}
</style>
