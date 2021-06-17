<template>
  <div class="card">
    <i class="bx text-6xl text-blue-700 text-center" :class="icon"></i>
    <div>
      <h2 class="text-center text-2xl font-semibold mb-2">{{ title }}</h2>
      <div class="p-2 text-center">{{ description }}</div>
    </div>
  </div>
</template>

<script>
export default {
  props: {
    title: String,
    description: String,
    icon: String,
  },
}
</script>

<style scoped>
.card {
  display: flex;
  flex-direction: column;
  gap: 1.25rem;
  max-width: 20rem;
  background-color: rgb(255 255 255);
  padding: 1.5rem;
  padding-bottom: 2.5rem;
  padding-top: 2.5rem;
  border-radius: 0.5rem;
  justify-content: center;

  --tw-shadow: 0 20px 25px -5px rgba(0, 0, 0, 0.1),
    0 10px 10px -5px rgba(0, 0, 0, 0.04);

  box-shadow: var(--tw-ring-offset-shadow, 0 0 #0000),
    var(--tw-ring-shadow, 0 0 #0000), var(--tw-shadow);
}
</style>
