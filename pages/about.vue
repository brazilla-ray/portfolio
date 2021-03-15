<template>
  <div class="grid-container">
    <page-header-vue class="page-header"></page-header-vue>
    <div class="content-wrapper">
      <div class="page-title">
        <h1>about me</h1>
      </div>
      <article class="main-content">
        <nuxt-content :document="page" />
      </article>
    </div>
  </div>
</template>

<script>
import PageHeaderVue from '~/components/PageHeader.vue'
export default {
  components: { PageHeaderVue },
  async asyncData({ $content }) {
    const page = await $content('about').fetch()

    return {
      page,
    }
  },
}
</script>

<style lang="scss" scoped>
.grid-container::after {
  background-color: $near-white;
  grid-column: 3/8;
}

.nuxt-content {
  line-height: 1.5;
}

.nuxt-content > p > a {
  color: $blue;
}
</style>
