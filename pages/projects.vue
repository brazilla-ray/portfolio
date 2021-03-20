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
}
</script>

<style lang="scss" scoped></style>
