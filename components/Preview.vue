<template>
  <div class="flex flex-col gap-3 sm:p-10 p-3 bg-dark">
    <h2 class="text-2xl font-semibold">{{ title }}</h2>
    <a :href="href" class="max-w-max">
      <img :src="img" width="600" />
    </a>
  </div>
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
