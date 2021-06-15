<template>
  <footer
    class="
      footer-background
      flex flex-col
      gap-5
      justify-center
      items-center
      text-white
      pb-10
    "
  >
    <div
      class="
        grid grid-cols-1
        md:grid-cols-3
        items-center
        justify-center
        gap-5
        mx-10
        py-10
      "
    >
      <div class="self-start">
        <h2 class="text-2xl pb-3">Our Pages</h2>
        <div class="flex flex-col text-lg">
          <a href="#">Home</a>
          <a href="#">About</a>
          <a href="#">Our Reccomendations</a>
        </div>
      </div>
      <div class="md:col-start-3 place-self-end">
        <h2 class="text-2xl pb-3">About Crypto Design</h2>
        <div class="text-lg">
          Usce eget justo eu eros dictum condimentum porta et quam. Nullam
          placerat dictum ullamcorper. Nulla velit ante, tincidunt id efficitur
          eu, vehicula sit amet quam. In nec viverra quam.
        </div>
      </div>
    </div>
    <div class="flex text-black text-2xl justify-center gap-5">
      <div class="p-2 w-10 h-10 flex items-center social">
        <a href="#">
          <i class="bx bxl-facebook"></i>
        </a>
      </div>
      <div class="p-2 w-10 h-10 flex items-center social">
        <a href="#">
          <i class="bx bxl-reddit"></i>
        </a>
      </div>
      <div class="p-2 w-10 h-10 flex items-center social">
        <a href="#">
          <i class="bx bxl-instagram"></i>
        </a>
      </div>
    </div>
    <div class="text-center">Copyright © 2021 - Crypto Design</div>
  </footer>
</template>

<style scoped>
.footer-background {
  background: linear-gradient(
    100deg,
    rgba(2, 39, 147, 1) 0%,
    rgba(4, 49, 173, 1) 53%,
    rgba(2, 57, 226, 1) 100%
  );
}

.social {
  background-color: white;
  border-radius: 9999px;
}

.social:hover {
  background-color: rgb(238, 172, 49);
}
</style>
