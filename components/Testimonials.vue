<template>
  <section>
    <!-- Testimonials -->
    <div
      class="
        reviews
        flex flex-col
        justify-center
        items-center
        my-10
        relative
        lg:px-20
        py-20
      "
    >
      <div class="flex flex-col w-5/6 text-center">
        <h1 class="text-white text-2xl">Testemonials</h1>
        <div class="text-white text-xl">
          Nullam facilisis finibus odio, a pellentesque urna pellentesque sit
          amet. In ultrices, nisl id sagittis interdum, ipsum lacus viverra
          arcu, a imperdiet sem metus in leo.
        </div>
      </div>
      <div
        class="grid md:grid-cols-3 grid-cols-1 lg:gap-10 gap-5 mt-20 sm:mx-10"
      >
        <div class="card">
          <i
            class="
              bx bx-message-square-detail
              text-6xl text-blue-700 text-center
            "
          ></i>
          <div>
            <h2 class="text-center text-xl">Loved It</h2>
            <div class="p-2 text-center">Donec posuere nec elit sed porta.</div>
          </div>
        </div>
        <div class="card">
          <i
            class="
              bx bx-message-square-detail
              text-6xl text-green-700 text-center
            "
          ></i>
          <div>
            <h2 class="text-center text-xl">Great Service</h2>
            <div class="p-2 text-center">Donec posuere nec elit sed porta.</div>
          </div>
        </div>
        <div class="card">
          <i
            class="
              bx bx-message-square-detail
              text-6xl text-red-700 text-center
            "
          ></i>
          <div>
            <h2 class="text-center text-xl">Wonderful Team</h2>
            <div class="p-2 text-center">Donec posuere nec elit sed porta.</div>
          </div>
        </div>
      </div>
      <div class="section-color"></div>
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

.section-color {
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
