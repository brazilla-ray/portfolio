<template>
  <div class="grid-container">
    <div class="indented">
      <header-vue site-title="ww"></header-vue>
    </div>
    <div class="full-width">
      <main-nav-vue></main-nav-vue>
    </div>
    <div class="content-wrapper mt-1 normal light">
      <p>
        Lorem ipsum dolor sit amet consectetur adipisicing elit. Atque ducimus
        praesentium totam consequuntur molestias, nemo molestiae a asperiores
        eius quam earum amet incidunt sed explicabo, iste ex temporibus dolorum
        sint!
      </p>
    </div>
  </div>
</template>

<script>
import HeaderVue from '~/components/Header.vue'
import MainNavVue from '~/components/MainNav.vue'

export default {
  components: { HeaderVue, MainNavVue },
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
  grid-column: 10/-1;
  grid-row: 2/-1;
  background-color: $near-white-quarter-trans;
  margin-right: -1em;
  padding: 1rem 2rem;
  border-left: 6px solid $near-black;
  z-index: -1;
}
</style>
