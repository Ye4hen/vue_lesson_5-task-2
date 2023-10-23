<template>
  <div>
    <product-roster :productsListData="notebooksList" />
  </div>
</template>

<script>
import ProductRoster from "./components/ProductRoster.vue";
import { notebooksList } from "./constants/3_data_notebooks";
export default {
  name: "App",
  components: { ProductRoster },
  data() {
    return {
      notebooksList,
    };
  },
};
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  /* text-align: center; */
  color: #2c3e50;
  margin-block: 60px;
}
</style>
