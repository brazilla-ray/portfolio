<template>
  <div class="grid-container">
    <div class="indented">
      <header-vue></header-vue>
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
}
</script>

<style lang="scss" scoped></style>
