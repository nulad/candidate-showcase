<template>
  <div id="app" class="container my-5">
    <h1>Candidate Showcase</h1>

    <div class="row">
      <Item
        v-for="item in candidates"
        :key="item.candidateId"
        :invId="item.candidateId"
        :name="item.name"
        :image="item.image"
        :dapil="item.dapil"
        :komisi="item.komisi"
        :summary="item.summary" />
    </div>
  </div>
</template>

<script>
require("bootstrap/dist/css/bootstrap.min.css");
import Item from "./Item.vue";

export default {
  name: "app",
  data() {
    return {
      candidates: [
        {
          candidateId: 1,
          name: "Ahmad Sahroni",
          image: "src/assets/ahmad-sahroni.png",
          dapil: "DKI Jakarta III",
          komisi: "III",
          summary: "lorem ipsum dolor sit amit2"
        },
        {
          invId: 2,
          name: "Ahmad Zainuddin",
          image: "src/assets/ahmad-zainuddin.jpg",
          dapil: "DKI Jakarta I",
          komisi: "IX",
          summary: "lorem ipsum dolor sit amit2"
        },
        {
          invId: 3,
          name: "Lucky Hakim",
          image: "src/assets/lucky-hakim.jpg",
          dapil: "Jawa Barat VI",
          komisi: "X",
          summary: "lorem ipsum dolor sit amit2"
        },
        {
          invId: 4,
          name: "Okky Asokawati",
          image: "src/assets/okky-asokawati.jpg",
          dapil: "DKI Jakarta II",
          komisi: "IX",
          summary: "lorem ipsum dolor sit amit2"
        }
      ]
    };
  },
  components: {
    Item
  }
};
</script>

<style>
#app {
  font-family: "Avenir", Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}

h1,
h2 {
  font-weight: normal;
}

ul {
  list-style-type: none;
  padding: 0;
}

li {
  display: inline-block;
  margin: 0 10px;
}

a {
  color: #42b983;
}
</style>
