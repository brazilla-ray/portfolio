<template>
  <article>
    <nuxt-content :document="page" />
  </article>
</template>

<script>
export default {
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
  width: 75%;
  margin: 35px auto 0;
}

.nuxt-content {
  line-height: 1.5;
}

.nuxt-content > h1 {
  color: #56b7eb;
}

.nuxt-content > p > a {
  color: #fffff0;
}
</style>
