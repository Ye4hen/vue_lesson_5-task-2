<template>
  <div class="container">
    <a :href="productData.link" class="img-container">
      <img :src="productData.imgSrc" />
    </a>
    <div class="main-content">
      <a :href="productData.link">
        <h3 class="title">{{ productData.title }}</h3>
      </a>
      <div v-if="productData.discount" class="discount">
        Ваша економія:
        <span class="discount-span">{{ productData.discount }}$</span>
      </div>
      <div class="main-bottom">
        <div class="prices">
          <div v-if="productData.oldPrice" class="old-price">
            {{ productData.oldPrice }} <span class="old-price-span">$</span>
          </div>
          <div class="price">
            {{ productData.price }}<span class="price-span">$</span>
          </div>
        </div>
        <button class="btn">Купити</button>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: "ProductCard",
  props: {
    productData: {
      type: Object,
      default: () => ({}),
    },
  },
};
</script>

<style lang="css" scoped>
a {
  text-decoration: none;
  color: inherit;
}

.container {
  display: flex;
  justify-content: center;
  /* align-items: stretch; */
}

.img-container img {
  width: 200px;
  height: 200px;
}
.main-content {
}
.title {
  color: blue;
  font-size: 20px;
  margin-bottom: 10px;
  max-width: 350px;
}
.title:hover {
  text-decoration: underline;
}
.discount-span {
  color: red;
}
.discount {
  margin-bottom: 20px;
}
.main-bottom {
  display: flex;
  align-items: end;
  justify-content: space-between;
}
.prices {
}
.old-price {
  color: #ccc;
  text-decoration: line-through;
  margin-bottom: 5px;
  font-size: 20px;
}
.old-price-span {
  font-size: 16px;
  text-decoration: none;
}
.price {
  color: red;
  font-size: 30px;
}
.price-span {
  font-size: 20px;
}
.btn {
  color: #fff;
  background-color: green;
  border: 1px solid green;
  padding: 5px 10px;
  border-radius: 6px;
  transition: all 0.3s ease 0s;
  cursor: pointer;
}
.btn:hover {
  color: green;
  background-color: #fff;
}
</style>
