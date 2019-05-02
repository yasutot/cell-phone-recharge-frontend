<template>
  <div class="sva">
    <div class="sva-card" v-bind:style="{ backgroundImage: 'url(' + data.image + ')' }">
      <div class="badge">ASSINE</div>
      <span class="sva-card-description"></span>
    </div>
    <div class="sva-gain">{{ data.gain }}</div>
    <div class="sva-description">{{ data.description }}</div>
  </div>
</template>

<script>
export default {
  name: "AppSva",
  props: ["data"]
};
</script>

<style scoped lang="scss">
.sva-card {
  height: 119px;
  border-radius: 4px;
}
.badge {
  height: 21px;
  background-color: #2f80ed;
  float: right;
  margin: 0.7rem;
  border-radius: 2px;
  font-family: Roboto;
  font-style: normal;
  font-weight: 500;
  font-size: 10px;
  line-height: 1.2rem;
  padding: 0.1rem 0.7rem;
  color: #ffffff;
}
</style>
