<template>
  <div>
    <Blue-Dream-Header />
    <div id="details"></div>
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
              <div class="p-2 text-center">
                Donec posuere nec elit sed porta.
              </div>
            </div>
          </div>
          <div class="card">
            <i class="bx bx-medal text-6xl text-green-700 text-center"></i>
            <div>
              <h2 class="text-center text-xl">Content</h2>
              <div class="p-2 text-center">
                Donec posuere nec elit sed porta.
              </div>
            </div>
          </div>
          <div class="card">
            <i class="bx bx-meteor text-6xl text-red-700 text-center"></i>
            <div>
              <h2 class="text-center text-xl">Content</h2>
              <div class="p-2 text-center">
                Donec posuere nec elit sed porta.
              </div>
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
            Quisque feugiat finibus magna, in finibus velit varius eu. Vivamus
            nec sapien risus. Donec blandit felis et interdum placerat. Aliquam
            vitae est sit amet ante convallis iaculis convallis vel dolor.
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
            Quisque feugiat finibus magna, in finibus velit varius eu. Vivamus
            nec sapien risus. Donec blandit felis et interdum placerat. Aliquam
            vitae est sit amet ante convallis iaculis convallis vel dolor.
          </div>
        </div>
        <i
          class="bx bx-timer text-red-400 text-center"
          style="font-size: 200px"
        ></i>
      </div>
    </section>
    <div id="testimonials"></div>
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
          <h1 class="text-white text-5xl pb-10">Testemonials</h1>
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
              <div class="p-2 text-center">
                Donec posuere nec elit sed porta.
              </div>
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
              <div class="p-2 text-center">
                Donec posuere nec elit sed porta.
              </div>
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
              <div class="p-2 text-center">
                Donec posuere nec elit sed porta.
              </div>
            </div>
          </div>
        </div>
        <div class="section-color"></div>
      </div>
    </section>
    <Contact />
    <Blue-Dream-Footer />
  </div>
</template>

<script>
export default {}
</script>

<style>
/* Sample `apply` at-rules with Tailwind CSS
.container {
@apply min-h-screen flex justify-center items-center text-center mx-auto;
}
*/
@import '@/assets/css/styles.css';

html {
  background-color: aliceblue;
  z-index: -50;
}
.container {
  margin: 0 auto;
  min-height: 100vh;
  display: flex;
  justify-content: center;
  align-items: center;
  text-align: center;
}

.title {
  font-family: 'Quicksand', 'Source Sans Pro', -apple-system, BlinkMacSystemFont,
    'Segoe UI', Roboto, 'Helvetica Neue', Arial, sans-serif;
  display: block;
  font-weight: 300;
  font-size: 100px;
  color: #35495e;
  letter-spacing: 1px;
}

.subtitle {
  font-weight: 300;
  font-size: 42px;
  color: #526488;
  word-spacing: 5px;
  padding-bottom: 15px;
}

.links {
  padding-top: 15px;
}

.reviews {
  background: url('~/assets/people.jpg');
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
