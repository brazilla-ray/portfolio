<template>
  <div class="grid-container">
    <div class="indented">
      <header class="flex-container flex-row">
        <header-vue tag-line="front end web,"></header-vue>
      </header>
    </div>
    <div class="full-width row-2">
      <main-nav-vue></main-nav-vue>
    </div>
  </div>
</template>

<script>
import HeaderVue from '~/components/Header.vue'
import MainNavVue from '~/components/MainNav.vue'
export default {
  components: {
    HeaderVue,
    MainNavVue,
  },
}
</script>

<style lang="scss" scoped></style>
