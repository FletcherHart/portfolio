<template>
  <section>
    <div class="flex justify-center">
      <div
        class="
          grid
          md:grid-cols-3
          grid-cols-1
          lg:gap-10
          gap-5
          -mt-10
          sm:mx-10
          z-10
        "
      >
        <div class="card">
          <i class="bx bx-coin-stack text-6xl text-blue-700 text-center"></i>
          <div>
            <h2 class="text-center text-xl">Content</h2>
            <div class="p-2 text-center">Donec posuere nec elit sed porta.</div>
          </div>
        </div>
        <div class="card">
          <i class="bx bx-medal text-6xl text-green-700 text-center"></i>
          <div>
            <h2 class="text-center text-xl">Content</h2>
            <div class="p-2 text-center">Donec posuere nec elit sed porta.</div>
          </div>
        </div>
        <div class="card">
          <i class="bx bx-meteor text-6xl text-red-700 text-center"></i>
          <div>
            <h2 class="text-center text-xl">Content</h2>
            <div class="p-2 text-center">Donec posuere nec elit sed porta.</div>
          </div>
        </div>
      </div>
    </div>
    <div
      class="
        flex
        sm:flex-row
        flex-col
        sm:gap-20
        gap-10
        sm:mx-20
        mx-10
        mt-20
        items-center
        justify-center
      "
    >
      <i
        class="bx bx-bulb text-yellow-400 text-center"
        style="font-size: 200px"
      ></i>
      <div>
        <h2 class="text-xl">Your Goals</h2>
        <div class="max-w-lg">
          Quisque feugiat finibus magna, in finibus velit varius eu. Vivamus nec
          sapien risus. Donec blandit felis et interdum placerat. Aliquam vitae
          est sit amet ante convallis iaculis convallis vel dolor.
        </div>
      </div>
    </div>
    <div
      class="
        flex
        sm:flex-row
        flex-col
        sm:gap-20
        gap-10
        sm:mx-20
        mx-10
        mt-20
        items-center
        justify-center
      "
    >
      <div>
        <h2 class="text-xl">Making a Plan</h2>
        <div class="max-w-lg">
          Quisque feugiat finibus magna, in finibus velit varius eu. Vivamus nec
          sapien risus. Donec blandit felis et interdum placerat. Aliquam vitae
          est sit amet ante convallis iaculis convallis vel dolor.
        </div>
      </div>
      <i
        class="bx bx-timer text-red-400 text-center"
        style="font-size: 200px"
      ></i>
    </div>
  </section>
</template>

<style scoped>
@import '@/assets/css/styles.css';

.reviews {
  background: url('/people.jpg');
  z-index: -2;
  background-size: cover;
}

.header-cover {
  position: absolute;
  top: 0;
  height: 100%;
  width: 100%;
  opacity: 80%;
  z-index: -1;
  background: linear-gradient(
    100deg,
    rgba(2, 39, 147, 1) 0%,
    rgba(4, 49, 173, 1) 53%,
    rgba(2, 57, 226, 1) 100%
  );
}
</style>
