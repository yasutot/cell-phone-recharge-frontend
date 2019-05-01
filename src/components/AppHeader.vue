<template>
  <div class="header">
    <div class="header-top pure-g">
      <div class="pure-u-1">
        <img id="logo" src="../assets/logo.png">
      </div>
      <div id="no-balance-text" class="pure-u-1 header-text">
        <span>você está sem saldo</span>
      </div>
      <div id="recharge-now-text" class="pure-u-1 header-text">
        <span>recarregue agora</span>
      </div>
      <div class="pure-u-1-2">
        <a class="card-link" href>
          <div class="card mr-05">
            <div class="card-header">R$15</div>
            <div class="card-body">E ganhe R$5,00 de bônus</div>
            <div class="card-bottom">CONTRATAR</div>
          </div>
        </a>
      </div>
      <div class="pure-u-1-2">
        <a class="card-link" href>
          <div class="card ml-05">
            <div class="card-header">R$15</div>
            <div class="card-body">E ganhe R$5,00 de bônus</div>
            <div class="card-bottom">CONTRATAR</div>
          </div>
        </a>
      </div>
    </div>
    <div class="header-bottom pure-g">
      <div class="pure-u-1-2">
        <a class="tab-button" href>créditos</a>
      </div>
      <div class="pure-u-1-2">
        <a class="tab-button" href>dados</a>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: "AppHeader"
};
</script>

<style scoped lang="scss">
.header {
  background: url("../assets/header-credits-bg.jpg");
  // height: 424px;
}
.header-top {
  padding: 1.5rem;
}
.header-text > span {
  font-family: "Titillium Web";
  font-style: normal;
  font-weight: bold;
  font-size: 14px;
  line-height: 14px; /* identical to box height */
  text-transform: uppercase;
  color: #ffffff;
  text-shadow: 0px 4px 4px rgba(0, 0, 0, 0.25);
}
#no-balance-text {
  padding-top: 1.5rem;
}
#recharge-now-text {
  margin-top: 0.5rem;
  margin-bottom: 3rem;
  span {
    font-style: normal;
    font-weight: normal;
    font-size: 36px;
    line-height: 37px;
  }
}
div.header-bottom > div {
  padding: 1rem 0 1rem;
  > a {
    display: block;
    width: 100%;
    height: 100%;
    text-align: center;
    font-family: "Titillium Web";
    font-style: normal;
    font-weight: bold;
    font-size: 14px;
    line-height: 0px;
    text-transform: uppercase;
    color: #f2f2f2;
  }
}
.card-link {
  // height: 100px;
  text-decoration: none;
  // margin-right: 0.5rem;
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
.mr-05 {
  margin-right: 0.5rem;
}
.ml-05 {
  margin-left: 0.5rem;
}
</style>
