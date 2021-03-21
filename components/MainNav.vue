<template>
  <nav class="flex-container flex-column mt-1">
    <div class="mt-1 box flex-container about">
      <NuxtLink to="/about" class="section-title">about</NuxtLink>
    </div>
    <div class="mt-1 box flex-container projects">
      <NuxtLink to="/projects" class="section-title">projects</NuxtLink>
    </div>
    <div class="mt-1 box flex-container contact">
      <NuxtLink to="/contact" class="section-title">contact</NuxtLink>
    </div>
  </nav>
</template>

<script>
export default {}
</script>

<style lang="scss" scoped>
.nuxt-link-exact-active {
  color: $near-black;
  border-bottom: none;
  font-size: 2.25rem;
}

.box {
  width: 150px;
  height: 150px;
  padding-left: 1rem;
}

.about {
  background-color: $near-white;
}

.projects {
  background-color: $blue;
}

.contact {
  background-color: $yellow;
}

.section-title {
  align-self: center;
}
</style>
