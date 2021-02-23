<template>
  <div class="container">
    <page-header-vue></page-header-vue>
    <h1 class="page-title">about me</h1>
    <article>
      <nuxt-content :document="page" />
    </article>
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

<style>
article {
  color: #fffff0;
}

.nuxt-content-container {
  margin-top: 17.5px;
}

.nuxt-content {
  line-height: 1.5;
}

.nuxt-content > p > a {
  color: #56b7eb;
}
</style>
