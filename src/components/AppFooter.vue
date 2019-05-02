<template>
  <div class="footer">
    <div class="pure-g" v-if="svas.length">
      <div class="pure-u-1-2" v-for="(item, index) in svas" :key="index">
        <div :class="index % 2 === 0 ? 'pr-03' : 'pl-03'">
          <AppSva :data="item"/>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
import AppSva from "./AppSva.vue";
export default {
  name: "AppFooter",
  components: {
    AppSva
  },
  data: () => {
    return {
      svas: []
    };
  },
  async mounted() {
    await this.getSva();
  },
  methods: {
    getSva() {
      fetch("https://tidal-hearing.glitch.me/sva")
        .then(response => response.json())
        .then(data => (this.svas = data))
        .catch(error => console.error(error));
    }
  }
};
</script>

<style scoped lang="scss">
.footer {
  padding: 2rem 1.5rem;
}
</style>
