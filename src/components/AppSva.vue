<template>
  <div class="sva">
    <a href class="sva-link">
      <div class="sva-card" v-bind:style="{ background: 'url(' + data.image + ') center' }">
        <div class="badge">ASSINE</div>
        <span class="sva-card-name">{{ data.name }}</span>
      </div>
      <div class="sva-gain">{{ data.gain }}</div>
      <div class="sva-description">{{ data.description }}</div>
    </a>
  </div>
</template>

<script>
export default {
  name: "AppSva",
  props: ["data"]
};
</script>

<style scoped lang="scss">
.sva-link {
  text-decoration: none;
}
.sva-card {
  background: linear-gradient(180deg, rgba(0, 0, 0, 0.0001) 0%, #000000 100%);
  background-size: cover !important;
  border-radius: 4px;
  box-shadow: 0px 1px 2px rgba(0, 0, 0, 0.1);
  height: 119px;
  mix-blend-mode: normal;
  position: relative;
  opacity: 0.9;
}
.badge {
  background-color: #2f80ed;
  border-radius: 2px;
  color: #ffffff;
  float: right;
  font-family: Roboto;
  font-size: 10px;
  font-style: normal;
  font-weight: 500;
  height: 21px;
  line-height: 1.2rem;
  margin: 0.7rem;
  padding: 0 0.7rem;
}
.sva-card-name {
  bottom: 0;
  color: #ffffff;
  font-family: Titillium Web;
  font-weight: 600;
  padding-bottom: 0.5rem;
  padding-left: 0.5rem;
  position: absolute;
}
.sva-gain {
  color: #000000;
  font-family: Roboto;
  font-weight: 600;
  padding: 0.5rem 0 0.5rem 0.5rem;
}
.sva-description {
  color: #000000;
  font-family: Roboto;
  font-size: 13px;
  font-weight: 300;
  line-height: 15px;
  margin-bottom: 1.5rem;
  padding-left: 0.5rem;
  text-transform: uppercase;
}
</style>
