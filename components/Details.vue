<template>
  <section class="relative flex justify-center h-80">
    <div
      class="grid sm:grid-cols-3 grid-cols-1 gap-10 absolute -top-10 sm:mx-20"
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
  </section>
</template>

<style scoped>
.card {
  display: flex;
  flex-direction: column;
  gap: 1.25rem;
  background-color: aliceblue;
  padding: 0.5rem;
  border-radius: 0.25rem;
  justify-content: center;

  --tw-shadow: 0 20px 25px -5px rgba(0, 0, 0, 0.1),
    0 10px 10px -5px rgba(0, 0, 0, 0.04);

  box-shadow: var(--tw-ring-offset-shadow, 0 0 #0000),
    var(--tw-ring-shadow, 0 0 #0000), var(--tw-shadow);
}
</style>
