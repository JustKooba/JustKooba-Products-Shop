<template>
  <div>
    <div class="input-container">
      <form>
        <input type="text" placeholder="Search Products" />
      </form>
    </div>
    <div class="carousel" v-dragscroll>
      <div class="item">
        <button>
          <img src="../../assets/phone.svg" alt=" Laptop icon" /> Phones
        </button>
      </div>
      <div class="item">
        <button>
          <img src="../../assets/laptop.svg" alt="laptop icon" /> Laptops
        </button>
      </div>
      <div class="item">
        <button>
          <img
            src="../../assets/perfume.svg"
            alt="perfume icon"
            class="perfume"
          />
          Perfumes
        </button>
      </div>
      <div class="item">
        <button>
          <img src="../../assets/oil.svg" alt="droplet icon" /> Oils
        </button>
      </div>
      <div class="item">
        <button>
          <img src="../../assets/care.svg" alt="heart with a plaster icon" />
          Care
        </button>
      </div>
      <div class="item">
        <button>
          <img src="../../assets/home.svg" alt="home icon" /> Home
        </button>
      </div>
      <div class="item">
        <button>
          <img src="../../assets/serum.svg" alt="pipette icon" /> Serums
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
};
</script>

<style></style>
