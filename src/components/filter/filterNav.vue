<template>
  <div class="container">
    <div class="input-container">
      <form>
        <input type="text" placeholder="Search Products" />
      </form>
    </div>
    <div class="carousel" v-dragscroll>
      <div class="item">
        <button ref="button" @click="sortProducts('smartphones')">
          <img src="../../assets/phone.svg" alt="Laptop icon" /> smartphones
        </button>
      </div>
      <div class="item">
        <button ref="button" @click="sortProducts('laptops')">
          <img src="../../assets/laptop.svg" alt="laptop icon" /> Laptops
        </button>
      </div>
      <div class="item">
        <button ref="button" @click="sortProducts('fragrances')">
          <img
            src="../../assets/perfume.svg"
            alt="perfume icon"
            class="perfume"
          />
          fragrances
        </button>
      </div>
      <div class="item">
        <button ref="button" @click="sortProducts('skincare')">
          <img src="../../assets/oil.svg" alt="droplet icon" /> skincare
        </button>
      </div>

      <div class="item">
        <button ref="button" @click="sortProducts('home-decoration')">
          <img src="../../assets/home.svg" alt="home icon" /> home-decoration
        </button>
      </div>
    </div>
  </div>
  <products-vue @sortProducts="handleSort" />
</template>

<script>
import { dragscroll } from "vue-dragscroll";
import productsVue from "../products/products.vue";

export default {
  name: "filterNav",
  directives: {
    dragscroll: dragscroll,
  },
  components: {
    productsVue,
  },
  data() {
    return {
      category: "",
    };
  },
  methods: {
    sortProducts(category) {
      this.category = category;
      console.log(this.category);
      this.$emit("sortProducts", this.category);
    },
  },
};
</script>

<style></style>
