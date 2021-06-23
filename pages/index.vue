<template>
  <div class="bg-home">
    <header class="flex flex-col justify-center items-center p-10 bg-dark">
      <h1 class="text-3xl font-bold text-center">
        Fletcher Hart's Frontend Portfolio
      </h1>
    </header>
    <main
      class="
        flex flex-col
        xl:flex-row-reverse
        gap-10
        justify-center
        p-5
        relative
      "
    >
      <section class="xl:w-max xl:block w-full flex justify-center">
        <div class="xl:sticky top-5 p-10 bg-dark w-full md:w-max">
          <div class="grid xl:grid-cols-1 sm:grid-cols-2 gap-5">
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
        </div>
      </section>
      <section
        class="
          grid grid-cols-1
          lg:justify-left
          place-items-center
          text-left
          gap-10
        "
      >
        <!-- Blue Dream -->
        <Preview
          :title="'Blue Dream'"
          :href="'./blue-dream'"
          :img="require('~/assets/blue-dream.jpg')"
        />
        <!-- Crypto Design -->
        <Preview
          :title="'Crypto Design'"
          :href="'./crypto-design'"
          :img="require('~/assets/crypto-design.jpg')"
        />
        <!-- Tracker -->
        <Preview
          :title="'Weight Tracker'"
          :href="'./tracker'"
          :img="require('~/assets/tracker.jpg')"
        />
      </section>
    </main>
    <footer
      class="bg-dark flex flex-col gap-5 justify-center text-white p-10 mt-10"
    >
      <div class="flex text-black text-2xl justify-center gap-5">
        <div class="p-2 w-10 h-10 flex items-center social">
          <a href="https://www.linkedin.com/in/fletcher-hart-b2006312b/">
            <i class="bx bxl-linkedin"></i>
          </a>
        </div>
        <div class="p-2 w-10 h-10 flex items-center social">
          <a href="https://github.com/FletcherHart">
            <i class="bx bxl-github"></i>
          </a>
        </div>
        <div class="p-2 w-10 h-10 flex items-center social">
          <a href="https://twitter.com/TheFailedDev">
            <i class="bx bxl-twitter"></i>
          </a>
        </div>
      </div>
      <div class="text-center">Copyright © 2021 - Fletcher Hart</div>
    </footer>
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

.skill:hover {
  transform: scale(1.1, 1.1);
  transition-property: transform;
  transition-timing-function: cubic-bezier(0.4, 0, 0.2, 1);
  transition-duration: 250ms;
  background-color: #f76369;
}

.social {
  color: #d1d1c2;
}

.social:hover {
  color: #f76369;
}

ul {
  display: flex;
  flex-direction: column;
  align-items: center;
}
</style>
