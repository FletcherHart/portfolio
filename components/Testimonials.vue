<template>
  <section class="flex flex-col justify-center items-center my-10 px-5">
    <h2 class="text-5xl font-bold text-blue-800 text-center">
      What People Are Saying
    </h2>
    <div class="my-5 md:w-3/5">
      <div id="tab1" class="flex flex-col tab text-center animate-left">
        <h3 class="text-2xl font-semibold">Vestibulum at molestie leo.</h3>
        <div>
          Praesent dictum, leo eget interdum tincidunt, tellus nulla scelerisque
          ex, vel tempus odio nulla nec mauris. Pellentesque ultrices felis ut
          elit ultrices tempor. Cras gravida leo elit, id pharetra arcu volutpat
          at. Duis et ante non ante elementum viverra. Morbi lobortis nisi eu
          feugiat faucibus.
        </div>
      </div>
      <div
        id="tab2"
        class="flex flex-col tab text-center animate-left"
        style="display: none"
      >
        <h3 class="text-2xl font-semibold">Cras pharetra velit dui.</h3>
        <div>
          Aenean a neque quam. Suspendisse vel hendrerit ex. Praesent bibendum
          tellus nulla, non congue metus rhoncus ut. Integer venenatis arcu eu
          pharetra gravida. Donec imperdiet, erat vel luctus molestie, lacus
          risus auctor nisi, tincidunt feugiat nunc turpis non mauris. Morbi
          pharetra dictum pellentesque.
        </div>
      </div>
      <div
        id="tab3"
        class="flex flex-col tab text-center animate-left"
        style="display: none"
      >
        <h3 class="text-2xl font-semibold">Nunc nec velit diam.</h3>
        <div>
          Nam laoreet ipsum at diam porta sollicitudin. Suspendisse ipsum nulla,
          consectetur sed turpis sit amet, efficitur tincidunt nulla. Integer
          euismod libero vel nunc venenatis, in tincidunt mi commodo. Donec orci
          enim, dapibus vitae tincidunt et, sagittis ut sem. Sed molestie,
          sapien eu tristique dictum, sapien libero mollis est, non luctus
          turpis ipsum dapibus orci.
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
