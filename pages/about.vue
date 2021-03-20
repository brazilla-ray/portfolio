<template>
  <div class="content">
    <header-vue></header-vue>
    <main-nav-vue></main-nav-vue>
  </div>
</template>

<script>
import HeaderVue from '~/components/Header.vue'
import MainNavVue from '~/components/MainNav.vue'

export default {
  components: { HeaderVue, MainNavVue },
  async asyncData({ $content }) {
    const page = await $content('about').fetch()

    return {
      page,
    }
  },
}
</script>

<style lang="scss" scoped></style>
