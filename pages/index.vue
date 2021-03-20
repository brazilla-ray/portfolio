<template>
  <div class="grid-container">
    <div class="indented">
      <header class="flex-container flex-row">
        <header-vue></header-vue>
        <sub-header-vue></sub-header-vue>
      </header>
    </div>
    <div class="full-width">
      <main-nav-vue></main-nav-vue>
    </div>
  </div>
</template>

<script>
import HeaderVue from '~/components/Header.vue'
import SubHeaderVue from '~/components/SubHeader.vue'
import MainNavVue from '~/components/MainNav.vue'
export default {
  components: {
    HeaderVue,
    SubHeaderVue,
    MainNavVue,
  },
}
</script>

<style lang="scss" scoped></style>
