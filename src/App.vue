<template>
  <div>
    <div id="app">
      <NavBar />
      <Todos />
      <StatusBar />
      <ProgressBar />
    </div>
  </div>
</template>

<script>
import Todos from "./components/Todos.vue";
import NavBar from "./components/NavBar.vue";
import StatusBar from "./components/StatusBar.vue";
import ProgressBar from "./components/ProgressBar.vue";
export default {
  name: "App",
  components: {
    Todos,
    NavBar,
    StatusBar,
    ProgressBar,
  },
};
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  background: rgb(219, 219, 219);
  margin: 20px auto;
  width: 90%;
  max-width: 800px;
}
</style>
