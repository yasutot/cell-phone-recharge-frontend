<template>
  <div :class="`header header-${selectedType}`">
    <div class="header-top pure-g">
      <div class="pure-u-1">
        <img id="logo" src="../assets/img/logo.png">
      </div>
      <div id="no-balance-text" class="pure-u-1 header-text">
        <span>você está sem saldo</span>
      </div>
      <div id="recharge-now-text" class="pure-u-1 header-text">
        <span>recarregue agora</span>
      </div>
      <div class="pure-u-1-2">
        <div class="pr-05">
          <AppHeaderCard v-if="selectedType" :value="this[selectedType][0]" :type="selectedType"/>
        </div>
      </div>
      <div class="pure-u-1-2">
        <div class="pl-05">
          <AppHeaderCard v-if="selectedType" :value="this[selectedType][1]" :type="selectedType"/>
        </div>
      </div>
    </div>
    <div class="header-bottom pure-g">
      <div class="pure-u-1-2">
        <AppTabButton
          :name="'créditos'"
          :isActive="selectedType==='credit'"
          v-on:clicked="tabButtonClick('credit')"
        />
      </div>
      <div class="pure-u-1-2">
        <AppTabButton
          :name="'dados'"
          :isActive="selectedType==='data'"
          v-on:clicked="tabButtonClick('data')"
        />
      </div>
    </div>
  </div>
</template>

<script>
import AppHeaderCard from "./AppHeaderCard.vue";
import AppTabButton from "./AppTabButton.vue";

export default {
  name: "AppHeader",
  components: {
    AppHeaderCard,
    AppTabButton
  },
  data: () => {
    return {
      selectedType: "",
      credit: [],
      data: []
    };
  },
  async mounted() {
    await this.getHeaderCardsData("credit");
  },
  methods: {
    tabButtonClick(type) {
      if (this.selectedType === type) return;

      if (this[type].length) {
        //prevents making another call if the data was already fetched
        this.selectedType = type;
      } else {
        this.getHeaderCardsData(type);
      }
    },
    getHeaderCardsData(type) {
      if (type === "credit") {
        var url = "https://tidal-hearing.glitch.me/recarga";
      } else {
        var url = "https://tidal-hearing.glitch.me/dados";
      }
      fetch(url)
        .then(response => response.json())
        .then(data => {
          this[type] = data;
          this.selectedType = type;
        })
        .catch(error => console.error(error));
    }
  }
};
</script>

<style scoped lang="scss">
.header-credit {
  background: url("../assets/img/header-credit-bg.png") center;
}
.header-data {
  background: url("../assets/img/header-data-bg.png") center;
}
.header {
  background-size: cover;
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
</style>
