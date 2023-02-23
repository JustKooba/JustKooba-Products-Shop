<template>
  <main>
    <header>
      <div class="user-greet">
        <img src="../../assets/profile-placeholder.svg" class="profile-pic" />
        <span>
          <p class="hello">Hello</p>
          <p class="user">Username</p>
        </span>
      </div>
      <hamburger />
    </header>
  </main>
</template>

<script>
import Hamburger from "../Hamburger/Hamburger.vue";

export default {
  name: "HeaderMain",
  components: {
    Hamburger,
  },
};
</script>

<style></style>
