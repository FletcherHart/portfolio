<template>
  <div class="bg-home">
    <header class="flex flex-col justify-center items-center p-10 bg-dark">
      <h1 class="text-3xl font-bold text-center">
        Fletcher Hart Frontend Portfolio
      </h1>
    </header>
    <main
      class="
        flex flex-col
        md:flex-row-reverse
        gap-10
        justify-center
        p-5
        relative
      "
    >
      <section class="md:sticky top-10 p-10 bg-dark w-full md:w-max h-2/3">
        <div class="grid grid-cols-1 gap-5">
          <!-- Languages -->
          <div>
            <h2 class="text-lg font-semibold mb-2">Languages</h2>
            <div class="flex flex-wrap gap-1">
              <div class="skill">HTML5</div>
              <div class="skill">CSS3</div>
              <div class="skill">JavaScript</div>
            </div>
          </div>
          <!-- Frameworks -->
          <div>
            <h2 class="text-lg font-semibold mb-2">Frameworks</h2>
            <div class="flex flex-wrap gap-1">
              <div class="skill">Vue.js</div>
              <div class="skill">Nuxt</div>
              <div class="skill">TailwindCSS</div>
            </div>
          </div>
          <!-- Version Control -->
          <div>
            <h2 class="text-lg font-semibold mb-2">
              Version Control & Hosting
            </h2>
            <div class="flex flex-wrap gap-1">
              <div class="skill">Git/Github</div>
              <div class="skill">Github Pages</div>
            </div>
          </div>
          <!-- Code Analysis -->
          <div>
            <h2 class="text-lg font-semibold mb-2">Linters & Formatters</h2>
            <div class="flex flex-wrap gap-1">
              <div class="skill">ESlint</div>
              <div class="skill">Commitlint</div>
              <div class="skill">Stylelint</div>
              <div class="skill">Prettier</div>
            </div>
          </div>
          <!-- Icons -->
          <div>
            <h2 class="text-lg font-semibold mb-2">Icons & Images</h2>
            <div class="flex flex-wrap gap-1">
              <div class="skill">Boxicons</div>
              <div class="skill">Pexels.com</div>
            </div>
          </div>
        </div>
      </section>
      <section
        class="grid grid-cols-1 justify-left items-left text-left gap-10"
      >
        <!-- Blue Dream -->
        <div class="flex flex-col gap-3 sm:p-10 p-3 bg-dark">
          <h2 class="text-2xl font-semibold">Blue Dream</h2>
          <a href="./blue-dream" class="max-w-max">
            <img src="~/assets/blue-dream.jpg" width="600" />
          </a>
        </div>
        <!-- Crypto Design -->
        <div class="flex flex-col gap-3 sm:p-10 p-3 bg-dark">
          <h2 class="text-2xl font-semibold">Crypto Design</h2>
          <a href="./crypto-design" class="max-w-max">
            <img src="~/assets/crypto-design.jpg" width="600" />
          </a>
        </div>
      </section>
    </main>
  </div>
</template>

<style scoped>
.bg-home {
  background-color: rgb(20, 20, 20);
  color: white;
}

.bg-dark {
  background-color: rgb(40, 40, 40);
}

li {
  border-radius: 50px;
  margin-bottom: 0.5rem;
  padding: 0.25rem;
  box-shadow: 0 0 0 2px #f76369;
  max-width: max-content;
}

.skill {
  border-radius: 50px;
  margin-bottom: 0.5rem;
  padding: 0.4rem;
  border: solid 2px #f76369;
  max-width: max-content;
}

ul {
  display: flex;
  flex-direction: column;
  align-items: center;
}
</style>
