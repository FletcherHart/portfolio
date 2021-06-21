<template>
  <section id="contact" class="my-20 flex flex-col justify-center items-center">
    <div class="flex flex-col text-center w-4/5">
      <h2 class="text-5xl pb-10">Contact Us</h2>
      <div class="text-lg">
        Nullam facilisis finibus odio, a pellentesque urna pellentesque sit
        amet. In ultrices, nisl id sagittis interdum, ipsum lacus viverra arcu,
        a imperdiet sem metus in leo.
      </div>
    </div>
    <div class="flex flex-col md:flex-row gap-5 justify-center my-10 w-4/5">
      <div class="md:w-1/3">
        <h3 class="text-xl">Stay in touch</h3>
        <div>
          Nullam facilisis finibus odio, a pellentesque urna pellentesque sit
          amet.
        </div>
      </div>
      <form class="flex flex-col gap-5 md:w-2/3">
        <div class="flex gap-5">
          <input
            id="name"
            name="name"
            placeholder="Full Name"
            class="p-3 rounded-xl w-1/2 shadow"
          />
          <input
            id="email"
            name="email"
            placeholder="Email"
            class="p-3 rounded-xl w-1/2 shadow"
          />
        </div>
        <textarea
          id="message"
          name="message"
          placeholder="Your Message"
          rows="5"
          class="p-3 rounded-xl shadow resize-none"
        ></textarea>
        <button
          type="submit"
          class="rounded-full bg-blue-600 text-white p-4 max-w-max"
        >
          Submit Message
        </button>
      </form>
    </div>
  </section>
</template>
