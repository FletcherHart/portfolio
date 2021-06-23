<template>
  <a
    :href="href"
    class="
      flex flex-col
      gap-3
      sm:p-10
      p-3
      bg-dark
      transition
      duration-500
      ease-in-out
      transform
      hover:-translate-y-1 hover:scale-105
      max-w-max
    "
  >
    <h2 class="text-2xl font-semibold">{{ title }}</h2>
    <img :src="img" width="600" heigth="297" />
  </a>
</template>

<script>
export default {
  props: {
    href: {
      type: String,
      default: '',
    },
    img: {
      type: String,
      default: '',
    },
    title: {
      type: String,
      default: '',
    },
  },
}
</script>
