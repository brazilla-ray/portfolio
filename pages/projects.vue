<template>
  <div class="grid-container">
    <div class="indented">
      <header-vue site-title="ww"></header-vue>
    </div>
    <div class="full-width">
      <main-nav-vue></main-nav-vue>
    </div>
    <div class="content behind">
      <main-content-vue
        page-style="projects-content"
        class="mt-1"
      ></main-content-vue>
    </div>
  </div>
</template>

<script>
import HeaderVue from '~/components/Header.vue'
import MainNavVue from '~/components/MainNav.vue'
import MainContentVue from '~/components/MainContent.vue'

export default {
  components: { HeaderVue, MainNavVue, MainContentVue },
}
</script>

<style lang="scss" scoped></style>
