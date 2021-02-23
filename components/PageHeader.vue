<template>
  <div>
    <header>
      <nav>
        <NuxtLink to="/">home</NuxtLink>
        <NuxtLink to="/about">about</NuxtLink>
        <NuxtLink to="/contact">contact</NuxtLink>
      </nav>
    </header>
  </div>
</template>

<script>
export default {}
</script>

<style scoped>
nav {
  display: flex;
  flex-flow: row wrap;
  justify-content: space-around;
}

nav > a {
  color: #fffff0;
}

.nuxt-link-active {
  color: #fffff0;
}

.nuxt-link-exact-active {
  color: #56b7eb;
}
</style>
