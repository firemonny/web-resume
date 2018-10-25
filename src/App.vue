<template>
  <div id="app">
    <resume />
  </div>
</template>

<script>
import resume from "./components/resume";
export default {
  name: "app",
  components: {
    resume
  }
};
</script>

<style>
#app {
  font-family: "Rokkitt", Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #000000;
  background-color: #f5f5dc;
  padding: 0;
  text-shadow: 1px 1px grey;
}
</style>
