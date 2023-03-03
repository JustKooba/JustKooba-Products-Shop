<template>
  <div class="container">
    <div class="input-container">
      <form>
        <input type="text" placeholder="Search Products" />
      </form>
    </div>
    <div class="carousel" v-dragscroll>
      <div class="item">
        <button ref="button" @click="sortProducts" v-on:click="handleClick">
          <img src="../../assets/phone.svg" alt="Laptop icon" /> smartphones
        </button>
      </div>
      <div class="item">
        <button ref="button" @click="sortProducts" v-on:click="handleClick">
          <img src="../../assets/laptop.svg" alt="laptop icon" /> Laptops
        </button>
      </div>
      <div class="item">
        <button ref="button" @click="sortProducts" v-on:click="handleClick">
          <img
            src="../../assets/perfume.svg"
            alt="perfume icon"
            class="perfume"
          />
          fragrances
        </button>
      </div>
      <div class="item">
        <button ref="button" @click="sortProducts" v-on:click="handleClick">
          <img src="../../assets/oil.svg" alt="droplet icon" /> skincare
        </button>
      </div>

      <div class="item">
        <button ref="button" v-on:click="handleClick" @click="sortProducts">
          <img src="../../assets/home.svg" alt="home icon" /> home-decoration
        </button>
      </div>
    </div>
  </div>
</template>

<script>
import { dragscroll } from "vue-dragscroll";
export default {
  name: "filterNav",
  directives: {
    dragscroll: dragscroll,
  },
  data() {
    return {
      category: "",
    };
  },
  methods: {
    sortProducts() {
      this.$emit("sortProducts", this.category);
    },
    handleClick() {
      
      this.category = event.target.innerText;
      console.log(this.category);
    },
  },
};
</script>

<style></style>
