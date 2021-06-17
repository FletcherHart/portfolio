<template>
  <div class="flex flex-col justify-center items-center py-10">
    <header class="flex flex-col justify-center items-center py-10">
      <h1 class="text-3xl font-bold">Fletcher Hart Frontend Portfolio</h1>
      <div class="grid grid-cols-1 md:grid-cols-3 gap-10 my-10 text-center">
        <!-- Languages -->
        <div>
          <h2 class="font-semibold">Languages</h2>
          <ul class="text-left">
            <li>HTML5</li>
            <li>CSS3</li>
            <li>JavaScript</li>
          </ul>
        </div>
        <!-- Frameworks -->
        <div>
          <h2 class="font-semibold">Frameworks</h2>
          <ul class="text-left">
            <li>Vue.js</li>
            <li>Nuxt</li>
            <li>TailwindCSS</li>
          </ul>
        </div>
        <!-- Version Control -->
        <div>
          <h2 class="font-semibold">Version Control & Hosting</h2>
          <ul class="text-left">
            <li>Git/Github</li>
            <li>Github Pages</li>
          </ul>
        </div>
        <!-- Code Analysis -->
        <div>
          <h2 class="font-semibold">Code Analysis & Correction</h2>
          <ul class="text-left">
            <li>ESlint</li>
            <li>Prettier</li>
          </ul>
        </div>
        <!-- Icons -->
        <div>
          <h2 class="font-semibold">Icons & Images</h2>
          <ul class="text-left">
            <li>Boxicons</li>
            <li>Pexels.com</li>
          </ul>
        </div>
      </div>
    </header>
    <main class="flex flex-col gap-10 justify-center items-center py-10">
      <!-- Blue Dream -->
      <div class="flex flex-col items-center gap-3">
        <h2 class="text-xl font-semibold">Blue Dream</h2>
        <a href="./blue-dream">
          <img src="~/assets/blue-dream.jpg" width="600" />
        </a>
      </div>
      <!-- Crypto Design -->
      <div class="flex flex-col items-center gap-3">
        <h2 class="text-xl font-semibold">Crypto Design</h2>
        <a href="./crypto-design">
          <img src="~/assets/crypto-design.jpg" width="600" />
        </a>
      </div>
    </main>
  </div>
</template>
