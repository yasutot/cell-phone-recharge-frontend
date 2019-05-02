<template>
  <div class="footer">
    <div class="pure-g">
      <div class="pure-u-1-2" v-if="svas.length" v-for="(item, index) in svas">
        <div :class="index % 2 === 0 ? 'pr-05' : 'pl-05'">
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
