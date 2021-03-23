<template>
  <div class="grid-container">
    <div class="indented">
      <header-vue site-title="ww"></header-vue>
    </div>
    <div class="full-width">
      <main-nav-vue></main-nav-vue>
    </div>
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
  data() {
    return {
      aboutPage: true,
    }
  },
}
</script>

<style lang="scss" scoped></style>
