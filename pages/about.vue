<template>
  <div class="grid-container">
    <div class="indented">
      <header-vue site-title="ww"></header-vue>
    </div>
    <div class="full-width">
      <main-nav-vue></main-nav-vue>
    </div>
    <div class="content content-wrapper mt-1">
      <main-content-vue></main-content-vue>
    </div>
  </div>
</template>

<script>
import HeaderVue from '~/components/Header.vue'
import MainNavVue from '~/components/MainNav.vue'
import MainContentVue from '~/components/MainContent.vue'

export default {
  components: { HeaderVue, MainNavVue, MainContentVue },
  async asyncData({ $content }) {
    const page = await $content('about').fetch()

    return {
      page,
    }
  },
}
</script>

<style lang="scss" scoped>
.content-wrapper {
  background-color: $near-white-quarter-trans;
  margin-right: -1em;
  padding: 1rem 2rem;
  border-left: 6px solid $near-black;
  z-index: -1;
}
</style>
