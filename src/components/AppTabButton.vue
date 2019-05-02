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
  background: transparent;
  border-top: 3px solid transparent;
  cursor: pointer;
  color: #f2f2f2;
  display: inline-block;
  font-family: "Titillium Web";
  font-size: 14px;
  font-style: normal;
  height: 100%;
  line-height: 3;
  outline: 1px solid rgba(242, 242, 242, 0.4);
  text-align: center;
  text-decoration: none;
  text-transform: uppercase;
  width: 100%;
}
.active {
  border-top: 3px solid white;
  font-weight: bold;
}
</style>