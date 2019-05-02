<template>
  <div id="app">
    <Home/>
  </div>
</template>

<script>
import Purecss from "purecss";
import Home from "./pages/Home.vue";

export default {
  name: "app",
  components: {
    Home
  }
};
</script>

<style lang="scss">
@import url("https://fonts.googleapis.com/css?family=Titillium+Web");
@import url("https://fonts.googleapis.com/css?family=Roboto");
@import "src/assets/stylesheets/style.scss";

#app {
  font-family: "Titillium Web", Arial;
}
// #app {
//   font-family: "Avenir", Helvetica, Arial, sans-serif;
//   -webkit-font-smoothing: antialiased;
//   -moz-osx-font-smoothing: grayscale;
//   text-align: center;
//   color: #2c3e50;
//   margin-top: 60px;
// }
</style>
