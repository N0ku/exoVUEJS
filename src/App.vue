<template>
  <mylist />
</template>

<script>
import mylist from "./components/coinlist.vue";

export default {
  name: "App",
  components: {
    mylist,
  }
};




/* const CoinGecko = require('coingecko-api');

//2. Initiate the CoinGecko API Client
const CoinGeckoClient = new CoinGecko();

//3. Make calls
var func = async () => {
  let data = await CoinGeckoClient.ping();
  return data;
};
console.log(func); */
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
