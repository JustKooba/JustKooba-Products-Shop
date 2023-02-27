<template>
  <div>
    <div
      class="product-card"
      v-for="product in products.data"
      :key="product.id"
    >
      <h1>Name:{{ product.title }}</h1>
      <img :src="product.images[0]" alt="Product Image" />
      <p>Desc:{{ product.description }}</p>
      <span>Price:{{ product.price }}</span>
    </div>
  </div>
</template>

<script>
import { reactive } from "vue";
import axios from "axios";
export default {
  name: "productsVue",
  setup() {
    const products = reactive({
      data: [],
    });
    async function fetchData() {
      try {
        const res = await axios.get("https://dummyjson.com/products");
        products.data = res.data.products;
        console.log(res.data);
      } catch (error) {
        console.error(error);
      }
    }
    fetchData();
    return {
      products,
    };
  },
};
</script>

<style></style>
