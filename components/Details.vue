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
          <img
            class="self-center"
            src="/icons/043-target.svg"
            width="75"
            height="75"
          />
          <div>
            <h2 class="text-center text-xl">Content</h2>
            <div class="p-2 text-center">Donec posuere nec elit sed porta.</div>
          </div>
        </div>
        <div class="card">
          <img
            class="self-center"
            src="/icons/043-target.svg"
            width="75"
            height="75"
          />
          <div>
            <h2 class="text-center text-xl">Content</h2>
            <div class="p-2 text-center">Donec posuere nec elit sed porta.</div>
          </div>
        </div>
        <div class="card">
          <img
            class="self-center"
            src="/icons/043-target.svg"
            width="75"
            height="75"
          />
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
      <img src="/icons/038-creativity.svg" width="200" height="200" />
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
      <img src="/icons/040-timer.svg" width="200" height="200" />
    </div>
    <!-- Testemonials -->
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
          <img
            class="self-center"
            src="/icons/043-target.svg"
            width="75"
            height="75"
          />
          <div>
            <h2 class="text-center text-xl">Content</h2>
            <div class="p-2 text-center">Donec posuere nec elit sed porta.</div>
          </div>
        </div>
        <div class="card">
          <img
            class="self-center"
            src="/icons/043-target.svg"
            width="75"
            height="75"
          />
          <div>
            <h2 class="text-center text-xl">Content</h2>
            <div class="p-2 text-center">Donec posuere nec elit sed porta.</div>
          </div>
        </div>
        <div class="card">
          <img
            class="self-center"
            src="/icons/043-target.svg"
            width="75"
            height="75"
          />
          <div>
            <h2 class="text-center text-xl">Content</h2>
            <div class="p-2 text-center">Donec posuere nec elit sed porta.</div>
          </div>
        </div>
      </div>
      <div class="header-cover"></div>
    </div>
  </section>
</template>

<style scoped>
.card {
  display: flex;
  flex-direction: column;
  gap: 1.25rem;
  max-width: 20rem;
  background-color: rgb(255, 255, 255);
  padding: 1.5rem;
  border-radius: 0.25rem;
  justify-content: center;

  --tw-shadow: 0 20px 25px -5px rgba(0, 0, 0, 0.1),
    0 10px 10px -5px rgba(0, 0, 0, 0.04);

  box-shadow: var(--tw-ring-offset-shadow, 0 0 #0000),
    var(--tw-ring-shadow, 0 0 #0000), var(--tw-shadow);
}

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
