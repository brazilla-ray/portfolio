<template>
  <div class="grid-container">
    <div class="indented">
      <header-vue tag-line="developing aspirations,"></header-vue>
    </div>
    <div class="full-width row-2">
      <main-nav-vue></main-nav-vue>
    </div>
    <div class="content row-2">
      <main-content-vue page-style="about-content">
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
  components: {
    HeaderVue,
    MainNavVue,
    MainContentVue,
    AboutContentVue,
  },
}
</script>

<style lang="scss" scoped></style>
