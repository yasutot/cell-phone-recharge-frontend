<template>
  <div class="home">
    <AppHeader/>
  </div>
</template>

<script>
import AppHeader from "../components/AppHeader.vue";

export default {
  name: "Home",
  components: {
    AppHeader
  }
};
</script>

<style scoped lang="scss">
.home {
  background-color: #e5e5e5;
}
</style>