<template>
  <div class="grid-container">
    <div class="indented">
      <header-vue site-title="ww"></header-vue>
    </div>
    <div class="full-width">
      <main-nav-vue></main-nav-vue>
    </div>
    <div class="content behind">
      <main-content-vue page-style="about-content" class="mt-1">
        <about-content-vue></about-content-vue>
      </main-content-vue>
    </div>
  </div>
</template>

<script>
import HeaderVue from '~/components/Header.vue'
import MainNavVue from '~/components/MainNav.vue'
import MainContentVue from '~/components/MainContent.vue'
import AboutContentVue from '~/components/AboutContent.vue'

export default {
  components: { HeaderVue, MainNavVue, MainContentVue, AboutContentVue },
  async asyncData({ $content }) {
    const page = await $content('about').fetch()

    return {
      page,
    }
  },
}
</script>

<style lang="scss" scoped></style>
