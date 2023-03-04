<template>
  <div>
    <header-main />
    <filter-nav />
  </div>
</template>

<script>
import HeaderMain from "./components/Header/Header.vue";
import filterNav from "./components/filter/filterNav.vue";
export default {
  components: {
    HeaderMain,
    filterNav,
  },
};
</script>

<style></style>
