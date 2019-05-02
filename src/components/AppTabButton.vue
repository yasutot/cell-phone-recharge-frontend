<template>
  <div>
    <a
      class="tab-button"
      :class="{ 'active': this.isActive }"
      v-on:click="$emit('clicked')"
    >{{ name }}</a>
  </div>
</template>

<script>
export default {
  name: "AppTabButton",
  props: ["name", "isActive"]
};
</script>

<style scoped lang="scss">
a {
  display: inline-block;
  width: 100%;
  height: 100%;
  text-align: center;
  font-family: "Titillium Web";
  font-style: normal;
  font-size: 14px;
  line-height: 3;
  text-transform: uppercase;
  color: #f2f2f2;
  background: transparent;
  outline: 1px solid rgba(242, 242, 242, 0.4);
  border-top: 3px solid transparent;
  text-decoration: none;
}
.active {
  font-weight: bold;
  border-top: 3px solid white;
}
.pt-1 {
  padding-top: 0.5rem;
  height: 100%;
  display: block;
}
.pb-1 {
  padding-bottom: 0.5rem;
}
</style>