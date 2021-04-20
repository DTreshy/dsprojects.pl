<template>
  <div>
    <nav class="flex px-32 py-5">
      <nuxt-link to="/">
        <div class="text-2xl font-bold">DSPROJECTS</div>
      </nuxt-link>
      <div class="block lg:hidden">
        <button class="flex items-center px-3 py-2 rounded-md">
          <svg
            class="fill-current h-3 w-3"
            viewBox="0 0 20 20"
            xmlns="http://www.w3.org/2000/svg"
          >
            <title>Menu</title>
            <path d="M0 3h20v2H0V3zm0 6h20v2H0V9zm0 6h20v2H0v-2z" />
          </svg>
        </button>
      </div>
      <div
        class="w-full block lg:items-center lg:w-auto float-right ml-auto text-xl"
      >
        <div
          v-for="item in menuItems"
          :key="item.text"
          class="block lg:inline-block px-5"
        >
          <nuxt-link
            to=""
            class="font-semibold hover:text-yellow-500 transition"
          >
            {{ item.text }}
          </nuxt-link>
        </div>
      </div>
    </nav>
    <Nuxt />
  </div>
</template>

<script>
export default {
  data() {
    return {
      menuItems: [
        { text: 'Portfolio' },
        { text: 'Download CV' },
        { text: 'Hire me' },
      ],
    }
  },
}
</script>
