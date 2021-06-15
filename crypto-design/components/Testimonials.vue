<template>
  <section class="flex flex-col justify-center items-center my-10 px-5">
    <h2 class="text-3xl font-bold text-blue-800 text-center">
      What People Are Saying
    </h2>
    <div class="my-5">
      <div id="tab1" class="flex flex-col tab text-center animate-left">
        <h3 class="text-2xl font-semibold">Vestibulum at molestie leo.</h3>
        <div>
          Nullam id laoreet metus. Nam ut risus finibus, vulputate magna id,
          tempor erat. Fusce sagittis ligula eget imperdiet dictum.
        </div>
      </div>
      <div
        id="tab2"
        class="flex flex-col tab text-center animate-left"
        style="display: none"
      >
        <h3 class="text-2xl font-semibold">Cras pharetra velit dui.</h3>
        <div>
          Praesent quam quam, maximus vel lacinia interdum, vulputate vel metus.
          Vivamus in pulvinar lectus.
        </div>
      </div>
      <div
        id="tab3"
        class="flex flex-col tab text-center animate-left"
        style="display: none"
      >
        <h3 class="text-2xl font-semibold">Nunc nec velit diam.</h3>
        <div>
          Nam eu eros vulputate velit tristique congue nec at mauris. Proin
          justo ante, accumsan ut iaculis non, maximus id ante.
        </div>
      </div>
    </div>
    <div>
      <button
        class="tabLink text-red-700 focus:outline-none"
        @click="changeTab('tab1', $event)"
      >
        <i class="bx bxs-circle"></i>
      </button>
      <button
        class="tabLink focus:outline-none"
        @click="changeTab('tab2', $event)"
      >
        <i class="bx bxs-circle"></i>
      </button>
      <button
        class="tabLink focus:outline-none"
        @click="changeTab('tab3', $event)"
      >
        <i class="bx bxs-circle"></i>
      </button>
    </div>
  </section>
</template>

<script>
export default {
  methods: {
    changeTab(tab, event) {
      const tabLinks = document.getElementsByClassName('tabLink')
      const tabList = document.getElementsByClassName('tab')
      for (let i = 0; i < tabList.length; i++) {
        tabList[i].style.display = 'none'
      }
      document.getElementById(tab).style.display = 'flex'

      for (let i = 0; i < tabLinks.length; i++) {
        tabLinks[i].className = tabLinks[i].className.replace(
          ' text-red-700',
          ''
        )
      }
      event.currentTarget.className += ' text-red-700'
    },
  },
}
</script>

<style scoped>
.animate-left {
  position: relative;
  animation: animateleft 0.4s;
}
@keyframes animateleft {
  from {
    left: -300px;
    opacity: 0;
  }
  to {
    left: 0;
    opacity: 1;
  }
}
</style>
