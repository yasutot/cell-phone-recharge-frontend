<template>
  <a class="card-link" href>
    <div class="card">
      <div
        class="card-header"
      >{{ this.type === "credit" ? `R$${this.value.amount}` : `${this.value.gb_amount}GB` }}</div>
      <div
        class="card-body"
      >{{ this.type === "credit" ? `E ganhe R$ ${this.value.bonus_amount} de bônus` : "Redes sociais Ilimitadas" }}</div>
      <div class="card-bottom">CONTRATAR</div>
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
  text-decoration: none;
  height: auto;
  .card {
    background-color: #f2f2f2;
    font-family: "Titillium Web";
    box-shadow: 0px 4px 34px rgba(0, 0, 0, 0.25);
    border-radius: 8px;
    text-align: center;
    .card-header {
      font-weight: bold;
      font-size: 36px;
      line-height: 55px;
      color: #2e7ce6;
    }
    .card-body {
      font-size: 10px;
      line-height: 15px;
      color: #828282;
      padding-bottom: 0.5rem;
    }
    .card-bottom {
      font-size: 14px;
      padding: 0.5rem;
      color: #55361a;
      background-color: #f2984a;
      border-radius: 0 0 8px 8px;
    }
  }
}
</style>
