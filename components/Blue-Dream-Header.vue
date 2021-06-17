<template>
  <header id="welcome" class="w-full flex justify-center relative header">
    <nav
      class="
        fixed
        w-5/6
        bg-white
        border-2 border-black
        rounded-3xl
        flex
        p-2
        px-10
        sm:justify-between
        justify-center
        mt-10
        z-50
      "
    >
      <div class="flex">
        <i
          class="bx bx-cube text-green-500 text-center"
          style="font-size: 50px"
        ></i>
        <div class="flex items-center">
          <a
            href="#welcome"
            class="text-green-700 text-xl px-2 py-2 rounded-xl font-semibold"
          >
            Blue Dream
          </a>
        </div>
      </div>
      <div class="sm:flex gap-5 items-center hidden">
        <a href="#details">About</a>
        <a href="#testimonials">Testimonials</a>
        <a href="#contact">Contact</a>
      </div>
    </nav>
    <div class="my-10 flex items-center justify-center z-10">
      <div class="flex flex-col w-5/6 text-center">
        <h1 class="text-white text-2xl">Lorem Ipsum</h1>
        <div class="text-white text-xl">
          Nullam facilisis finibus odio, a pellentesque urna pellentesque sit
          amet. In ultrices, nisl id sagittis interdum, ipsum lacus viverra
          arcu, a imperdiet sem metus in leo. Nullam euismod, est id lacinia
          blandit, lectus sapien vestibulum tortor, et pharetra blandit magna.
          Nunc ultricies dui condimentum, venenatis libero gravida, venenatis
          tortor.
        </div>
      </div>
    </div>
    <div class="header-cover"></div>
  </header>
</template>

<style scoped>
.header {
  background: url('~/assets/geo.jpg');
  background-repeat: no-repeat;
  background-size: 100% 100%;
  height: 40rem;
}

.header-cover {
  position: absolute;
  top: 0;
  height: 100%;
  width: 100%;
  opacity: 60%;
  z-index: 1;
  background: linear-gradient(
    100deg,
    rgba(2, 39, 147, 1) 0%,
    rgba(4, 49, 173, 1) 53%,
    rgba(2, 57, 226, 1) 100%
  );
}
</style>
