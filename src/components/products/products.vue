<template>
  <div class="products-container">
    <div
      class="product-card"
      v-for="product in products.data"
      :key="product.id"
      :style="{ display: productDisplay }"
    >
      <img :src="product.images[0]" alt="Product Image" />

      <div class="right">
        <h1>{{ product.title }}</h1>
        <p>currently in stock: {{ product.stock }}</p>
        <span>{{ product.price }}$</span>
      </div>
    </div>
  </div>
  <div class="error" :style="{ display: errorDisplay }">
    <h1>The service is currently unaviable. please try again later.</h1>
  </div>
</template>

<script>
import { reactive } from "vue";
import axios from "axios";

export default {
  data() {
    return {
      productDisplay: "flex",
      errorDisplay: "none",
      category: "",
    };
  },

  name: "productsVue",
  methods: {
    handleSort(category) {
      this.category = category;
      console.log("Sorting by category: ", this.category);
    },
  },

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
        this.errorDisplay = "flex";
      }
    }
    fetchData();
    return {
      products,
    };
  },
};
</script>
