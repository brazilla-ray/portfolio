<template>
  <div>
    <header>
      <nav>
        <NuxtLink to="/">home</NuxtLink>
        <NuxtLink to="/about">about</NuxtLink>
        <NuxtLink to="/projects">projects</NuxtLink>
        <NuxtLink to="/contact">contact</NuxtLink>
      </nav>
    </header>
  </div>
</template>

<script>
export default {}
</script>

<style lang="scss" scoped>
nav {
  display: flex;
  flex-flow: row wrap;
  justify-content: space-between;
}

nav > a {
  color: $near-white;
}

.nuxt-link-active {
  color: $near-white;
}

.nuxt-link-exact-active {
  color: #56b7eb;
}
</style>
