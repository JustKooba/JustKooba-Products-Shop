<template>
  <div>
    <header-main />
    <filter-nav />
    <products-vue />
  </div>
</template>

<script>
import HeaderMain from "./components/Header/Header.vue";
import filterNav from "./components/filter/filterNav.vue";
import productsVue from "./components/products/products.vue";
export default {
  components: {
    HeaderMain,
    filterNav,
    productsVue,
  },
};
</script>

<style></style>
