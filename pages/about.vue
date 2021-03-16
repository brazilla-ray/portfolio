<template>
  <div class="grid-container">
    <page-header-vue class="page-header"></page-header-vue>
    <div class="page-title">
      <h1>about me</h1>
    </div>
    <div class="content-wrapper">
      <article class="main-content">
        <img src="~/static/self.png" alt="self-portrait" class="inline-image" />
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

.inline-image {
  max-width: 31.25vw;
  margin: 0 1em 1em 0;
  float: left;
}

@media screen and (min-width: 568px) {
  .inline-image {
    margin: 0 2em 2em 0;
  }
}
</style>
