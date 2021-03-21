<template>
  <div class="mt-1">
    <NuxtLink to="/">
      <h1 class="title large">{{ siteTitle }}</h1>
    </NuxtLink>
  </div>
</template>

<script>
export default {
  props: {
    siteTitle: {
      type: String,
      default: 'william whitaker',
    },
  },
}
</script>

<style lang="scss" scoped>
.nuxt-link-active,
.nuxt-link-exact-active {
  text-decoration: none;
}
</style>
