<template>
  <a class="card-link" href>
    <div class="card">
      <div
        class="card-header"
      >{{ this.type === "credit" ? `R$${this.value.amount}` : `${this.value.gb_amount}GB` }}</div>
      <div
        class="card-body"
      >{{ this.type === "credit" ? `E ganhe R$${this.value.bonus_amount} de bônus` : "Redes sociais Ilimitadas" }}</div>
      <div class="card-bottom">contratar</div>
    </div>
  </a>
</template>

<script>
export default {
  name: "AppHeaderCard",
  props: ["type", "value"]
};
</script>

<style scoped lang="scss">
.card-link {
  height: auto;
  text-decoration: none;
  .card {
    background-color: #f2f2f2;
    border-radius: 8px;
    box-shadow: 0px 4px 34px rgba(0, 0, 0, 0.25);
    font-family: "Titillium Web";
    text-align: center;
    .card-header {
      color: #2e7ce6;
      font-size: 36px;
      font-weight: bold;
      line-height: 55px;
    }
    .card-body {
      color: #828282;
      font-size: 10px;
      line-height: 15px;
      padding-bottom: 0.5rem;
    }
    .card-bottom {
      background-color: #f2984a;
      border-radius: 0 0 8px 8px;
      color: #55361a;
      font-size: 14px;
      padding: 0.4rem;
      text-transform: uppercase;
    }
  }
}
</style>
