<template>
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
          <button type="submit" class="font-semibold p-3 min-w-max">
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
      <div class="banner-cover"></div>
    </div>
  </header>
</template>

<style scoped>
.bg-banner {
  position: relative;
  background: url('/bitcoin-color.jpg');
  background-repeat: no-repeat;
  background-size: cover;
  height: 40rem;
  width: 100%;
}

.banner-cover {
  position: absolute;
  top: 0;
  height: 100%;
  width: 100%;
  opacity: 0%;
  background-color: rgb(22, 0, 117);
}

.bg-search {
  background-color: rgba(255, 255, 255, 0.8);
}

.bg-search-header {
  background-color: rgba(22, 0, 117, 0.45);
}

button {
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
