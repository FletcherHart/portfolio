<template>
  <header class="w-full flex justify-center">
    <div
      class="
        w-5/6
        bg-white
        border-2 border-black
        rounded-3xl
        flex
        p-2
        px-10
        sm:justify-between
        justify-center
      "
    >
      <div class="flex">
        <Logo />
        <div class="flex items-center">
          <h1 class="text-white bg-green-600 px-2 py-2 rounded-xl">Brand</h1>
        </div>
      </div>
      <nav class="sm:flex gap-5 items-center hidden">
        <a href="#">Link 1</a>
        <a href="#">Link 2</a>
        <a href="#">Link 3</a>
      </nav>
    </div>
  </header>
</template>
