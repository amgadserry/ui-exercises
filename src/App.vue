<template>
  <div  class="c-grid-wrapper">
    <grid :rows="5" :cols="5"/>
  </div>
</template>

<script>
import Grid from "./components/grid/index.vue";
export default {
  name: "App",
  components: {
    Grid,
  },
};
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin: 0px;
  width: 100vw;
  height: 100vh;
}
</style>

<style scoped>
  .c-grid-wrapper {
    min-width: 100%;
    min-height: 100%;
    display: flex;
    justify-content: center;
    align-items: center;
  }
  .c-grid-wrapper .c-grid {
    min-width: 40%;
  }
</style>
