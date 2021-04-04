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
    <div class="secondary-nav row-2 col-13">
      <nav class="flex-container flex-column">
        <a href="https://twitter.com/w0whitaker" class="link">twitter</a>
        <a href="https://github.com/brazilla-ray" class="link mt-2">github</a>
        <a href="https://codepen.io/w0whitaker" class="link mt-2">codepen</a>
        <a
          href="https://www.linkedin.com/in/william-whitaker-4230bbab/"
          class="link mt-2"
        >
          linkedin</a
        >
        <a href="https://williamwhitaker.art" class="link mt-2">art</a>
      </nav>
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

<style lang="scss" scoped>
.secondary-nav {
  margin-top: 6.75rem;
}
</style>
