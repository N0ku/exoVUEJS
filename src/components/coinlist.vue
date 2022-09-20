<template>
  <h1>Hey</h1>
  <p>{{ getTime() }}</p>
  <div class="row" v-for="dataList in apiData" :key="dataList">
    <ul v-for="data in dataList" :key="data">
      <li>
        {{ apiData }}
      </li>
    </ul>
  </div>
</template>

<script>
/* import axios from "axios";
 */
export default {
  // eslint-disable-next-line vue/multi-word-component-names
  name: "coinlist",
  data() {
    return {
      localTime: "00H00min00s",
      apiData: "",
    };
  },
  methods: {
    getData() {
      this.requete();
    },
    clock() {
      setInterval(function () {
        var date = new Date();

        var hours = date.getHours();
        var minutes = date.getMinutes();
        var secondes = date.getSeconds();

        var time = `${hours}H${minutes}min${secondes}s`;
        this.localTime = time;
        console.log(this.localTime);
      }, 1000);
    },
    requete() {
      console.log("coucou");
      /*  axios.get("https://api.coingecko.com/api/v3/coins/")
       .then(json => this.apiData = json);   */
      /*  fetch("https://api.coingecko.com/api/v3/coins/")
        .then((result) => result.json())
        .then((json) => (this.apiData = json)); */
    },
    getTime() {
      return this.localTime;
    },
  },
  created() {
    this.requete();
  },
  beforeUnmount() {
    clearInterval(1000);
  },
};
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
</style>
