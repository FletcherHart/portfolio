<template>
  <footer
    class="footer-background flex flex-col gap-5 justify-center text-white h-60"
  >
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
    <div class="text-center">Copyright © 2021 - Blue Dream</div>
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
