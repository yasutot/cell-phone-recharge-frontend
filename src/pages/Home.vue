<template>
  <div class="home">
    <AppHeader/>
    <AppFooter/>
  </div>
</template>

<script>
import AppHeader from "../components/AppHeader.vue";
import AppFooter from "../components/AppFooter.vue";

export default {
  name: "Home",
  components: {
    AppHeader,
    AppFooter
  }
};
</script>