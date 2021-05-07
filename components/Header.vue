<template>
  <div class="mt-1">
    <header>
      <NuxtLink to="/">
        <h1 class="title large">william whitaker</h1>
        <p class="title sub mt-1">{{ tagLine }}</p>
      </NuxtLink>
    </header>
  </div>
</template>

<script>
export default {
  props: {
    tagLine: {
      type: String,
      default: '',
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
