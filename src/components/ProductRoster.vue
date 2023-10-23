<template>
  <div class="secondary-container">
    <product-card
      v-for="product in productsListData"
      :key="product.id"
      :productData="product"
    />
  </div>
</template>

<script>
import ProductCard from "./ProductCard.vue";
export default {
  name: "ProductRoster",

  components: { ProductCard },

  props: {
    productsListData: {
      type: Array,
      default: () => [],
    },
  },
};
</script>

<style lang='css' scoped>
.secondary-container {
  display: flex;
  flex-direction: column;
  gap: 50px;
}
</style>