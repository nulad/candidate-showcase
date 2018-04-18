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
import candidates from "./candidates";

export default {
  name: "app",
  data() {
    return {
      candidates: candidates
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
