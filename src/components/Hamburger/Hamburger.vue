<template>
  <div class="menu">
    <img src="../../assets/menu.svg" class="menu" @click="handleMenu" />
    <div class="content-menu" :style="{ display: menuDisplay }">
      <p>
        TODO Lorem ipsum dolor sit amet consectetur adipisicing elit.
        Accusantium earum tempora
      </p>
    </div>
  </div>
</template>

<script>
export default {
  name: "Hamburger",
  data() {
    return {
      menuDisplay: "none",
    };
  },
  methods: {
    handleMenu() {
      if (this.menuDisplay == "none") {
        this.menuDisplay = "block";
      } else if (this.menuDisplay == "block") {
        this.menuDisplay = "none";
      }
    },
  },
};
</script>

<style></style>
