<template>
  <div class="content">
    <header class="flex-container flex-row">
      <header-vue></header-vue>
      <sub-header-vue></sub-header-vue>
    </header>
    <div>
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

<style lang="scss" scoped>
header {
  margin: 1em 1em 0;
}
</style>
