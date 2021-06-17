<template>
  <div class="flex flex-col bg-gray-100">
    <Navbar />
    <header id="welcome" class="w-full flex justify-center mb-10">
      <div class="bg-banner flex items-center justify-center">
        <form
          class="
            z-50
            flex flex-col
            gap-10
            md:w-3/5
            w-4/5
            items-center
            justify-center
          "
        >
          <h1
            class="
              font-bold
              text-4xl text-white
              bg-search-header
              p-2
              border-2 border-white
              flex
              itemse-center
              min-w-max
            "
          >
            <label for="search">Search for Crypto</label>
          </h1>
          <div class="flex flex-col md:flex-row gap-3 w-full">
            <input
              name="search"
              placeholder="Enter crypto name here"
              class="p-3 w-full bg-search bg-transparent border border-white"
            />
            <button type="submit" class="font-semibold p-3 min-w-max search">
              Search Crypto
            </button>
          </div>
          <div class="flex gap-10 flex-col md:flex-row">
            <div class="flex flex-col bg-white text-center rounded p-2">
              <label for="price" class="font-semibold">Price</label>
              <select
                id="price"
                name="price"
                class="p-1 rounded border border-gray-400"
              >
                <option value="under1">Under $1</option>
                <option value="1to10">$1 - $10</option>
                <option value="10to50">$10 - $50</option>
                <option value="50to500">$50 - $500</option>
                <option value="over500">Over $500</option>
              </select>
            </div>
            <div class="flex flex-col bg-white text-center rounded p-2">
              <label for="sort" class="font-semibold">Sort by</label>
              <select
                id="sort"
                name="sort"
                class="p-1 rounded border border-gray-400"
              >
                <option value="oldest">Oldest</option>
                <option value="newest">Newest</option>
              </select>
            </div>
            <div class="flex flex-col bg-white text-center rounded p-2">
              <label for="hash" class="font-semibold">Hash Function</label>
              <select
                id="hash"
                name="has"
                class="p-1 rounded border border-gray-400"
              >
                <option value="sha-256">SHA-256</option>
                <option value="scrypt">scrypt</option>
              </select>
            </div>
          </div>
        </form>
      </div>
    </header>
    <section class="flex flex-col items-center justify-center my-10">
      <h2 class="text-5xl text-blue-800 mb-5 font-bold">
        Everything You Need to Know
      </h2>
      <div class="flex flex-col lg:flex-row gap-10 py-10 items-stretch">
        <Card
          title="Mining & You"
          description="This is placeholder text. If reusing this design, please replace this text with some content."
          icon="bx-code-block"
        />
        <Card
          title="GitHub"
          description="This design was created by Fletcher Hart. More of my work is available on my GitHub."
          icon="bx-envelope"
        />
        <Card
          title="The Tech Behind the Phenomenon"
          description="This is placeholder text. If reusing this design, please replace this text with some content."
          icon="bx-data"
        />
      </div>
    </section>
    <section class="flex flex-col justify-center items-center my-10 px-5">
      <h2 class="text-5xl font-bold text-blue-800 text-center">
        What People Are Saying
      </h2>
      <div class="my-5 md:w-3/5">
        <div id="tab1" class="flex flex-col tab text-center animate-left">
          <h3 class="text-2xl font-semibold">Vestibulum at molestie leo.</h3>
          <div>
            Praesent dictum, leo eget interdum tincidunt, tellus nulla
            scelerisque ex, vel tempus odio nulla nec mauris. Pellentesque
            ultrices felis ut elit ultrices tempor. Cras gravida leo elit, id
            pharetra arcu volutpat at. Duis et ante non ante elementum viverra.
            Morbi lobortis nisi eu feugiat faucibus.
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
            Nam laoreet ipsum at diam porta sollicitudin. Suspendisse ipsum
            nulla, consectetur sed turpis sit amet, efficitur tincidunt nulla.
            Integer euismod libero vel nunc venenatis, in tincidunt mi commodo.
            Donec orci enim, dapibus vitae tincidunt et, sagittis ut sem. Sed
            molestie, sapien eu tristique dictum, sapien libero mollis est, non
            luctus turpis ipsum dapibus orci.
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
    <Contact />
    <Footer />
  </div>
</template>

<script>
export default {
  components: {},
  data() {
    return {
      open: false,
      flex: false,
      'flex-col': false,
      hidden: true,
    }
  },
  computed: {
    mobileLinks() {
      return {
        flex: this.open,
        'flex-col': this.open,
        hidden: !this.open,
      }
    },
  },
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

<style>
/* Sample `apply` at-rules with Tailwind CSS
.container {
@apply min-h-screen flex justify-center items-center text-center mx-auto;
}
*/
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

.container {
  margin: 0 auto;
  min-height: 100vh;
  display: flex;
  justify-content: center;
  align-items: center;
  text-align: center;
}

.bg-banner {
  position: relative;
  background: url('~/assets/bitcoin-color.jpg');
  background-repeat: no-repeat;
  background-size: cover;
  height: 40rem;
  width: 100%;
}

.bg-search {
  background-color: rgba(255, 255, 255, 0.8);
}

.bg-search-header {
  background-color: rgba(22, 0, 117, 0.45);
}

.search {
  background-color: gold;
}

option {
  padding: 0.25rem;
}

::placeholder {
  /* Chrome, Firefox, Opera, Safari 10.1+ */
  color: black;
  opacity: 1; /* Firefox */
}
</style>
