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
          <NuxtLink
            to="/"
            class="text-gold text-xl px-2 py-2 rounded-xl font-semibold"
          >
            Crypto Design
          </NuxtLink>
        </div>
      </div>
      <div class="sm:flex gap-5 items-center hidden">
        <NuxtLink to="#details" class="header-link">About</NuxtLink>
        <NuxtLink to="#testimonials" class="header-link">Testimonials</NuxtLink>
        <NuxtLink to="#contact" class="header-link">Contact</NuxtLink>
      </div>
      <!--Mobiel-->
      <button class="sm:hidden" @click="open = !open">
        <i class="bx bx-menu p-2" style="font-size: 50px"></i>
      </button>
    </div>
    <div class="gap-5" :class="mobileLinks">
      <NuxtLink to="#details" class="header-link">About</NuxtLink>
      <NuxtLink to="#testimonials" class="header-link">Testimonials</NuxtLink>
      <NuxtLink to="#contact" class="header-link">Contact</NuxtLink>
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
