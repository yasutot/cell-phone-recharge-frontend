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
@import "src/assets/stylesheets/style.scss";

#app {
  font-family: "Titillium Web", Arial;
}
</style>
