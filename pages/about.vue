<template>
  <div class="grid-container">
    <page-header-vue class="page-header"></page-header-vue>
    <div class="content-wrapper">
      <h1 class="page-title">about me</h1>
      <article>
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
.grid-container::before {
  background: linear-gradient(45deg, $near-black, $near-white-trans);
}

.page-title {
  background-color: $near-white-quarter-trans;
}

article {
  color: $near-white;
}

.nuxt-content-container {
  margin-top: 6.25vh;
  width: 75vw;
}

.nuxt-content {
  line-height: 1.5;
}

.nuxt-content > p > a {
  color: #56b7eb;
}
</style>
