<template>
  <nav
    class="
      w-full
      bg-bitcoin
      text-gold
      font-semibold
      p-2
      sm:px-10
      justify-between
    "
  >
    <div class="flex justify-between">
      <div class="flex">
        <i
          class="bx bx-money text-gold text-center"
          style="font-size: 50px"
        ></i>
        <div class="flex items-center">
          <a
            href="#welcome"
            class="text-gold text-xl px-2 py-2 rounded-xl font-semibold"
          >
            Crypto Design
          </a>
        </div>
      </div>
      <div class="sm:flex gap-5 items-center hidden">
        <a class="header-link" href="#details">About</a>
        <a class="header-link" href="#testimonials">Testimonials</a>
        <a class="header-link" href="#contact">Contact</a>
      </div>
      <!--Mobiel-->
      <button class="sm:hidden" @click="open = !open">
        <i class="bx bx-menu p-2" style="font-size: 50px"></i>
      </button>
    </div>
    <div class="gap-5" :class="mobileLinks">
      <a class="header-link" href="#details">About</a>
      <a class="header-link" href="#testimonials">Testimonials</a>
      <a class="header-link" href="#contact">Contact</a>
    </div>
  </nav>
</template>

<script>
export default {
  data() {
    return {
      open: false,
      flex: false,
      'flex-col': false,
      hidden: true,
    }
  },
  computed: {
    mobileLinks() {
      return {
        flex: this.open,
        'flex-col': this.open,
        hidden: !this.open,
      }
    },
  },
}
</script>

<style scoped>
.bg-bitcoin {
  background-color: darkblue;
}

.header-link {
  border-right: solid 2px transparent;
  padding: 0.5rem;
}

.header-link:hover {
  background-color: white;
  color: black;

  --tw-border-opacity: 1;

  border-color: rgba(96, 165, 250, var(--tw-border-opacity));
}

.text-gold {
  color: gold;
}
</style>
