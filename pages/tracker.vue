<template>
  <div class="flex flex-col bg-color min-h-screen">
    <header class="font-bold text-4xl text-center py-10">Weight Tracker</header>
    <main>
      <client-only>
        <LineChart />
      </client-only>
    </main>
  </div>
</template>

<style>
.bg-color {
  background-color: rgb(238, 238, 238);
}
</style>
