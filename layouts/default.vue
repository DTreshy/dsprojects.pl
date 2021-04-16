<template>
  <div>
    <nav class="flex px-32 py-6">
      <div class="text-grey-800 text-2xl font-bold">DSPROJECTS</div>
      <div
        class="w-full block lg:items-center lg:w-auto float-right ml-auto text-xl"
      >
        <div>
          <a
            v-for="item in menuItems"
            :key="item.text"
            href="#responsive-header"
            class="block mt-4 lg:inline-block lg:mt-0 text-teal-200 hover:text-white px-6"
          >
            {{ item.text }}
          </a>
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
