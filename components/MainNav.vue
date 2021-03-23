<template>
  <nav class="mt-1">
    <div
      v-if="currentPageName === 'about'"
      class="flex-container flex-centered box about"
    >
      <h2>about</h2>
    </div>
    <div v-else class="flex-container flex-centered box">
      <NuxtLink to="/about" class="link">about</NuxtLink>
    </div>
    <div
      v-if="currentPageName === 'projects'"
      class="flex-container flex-centered box projects"
    >
      <h2>projects</h2>
    </div>
    <div v-else class="flex-container flex-centered box">
      <NuxtLink to="/projects" class="link">projects</NuxtLink>
    </div>
    <div
      v-if="currentPageName === 'contact'"
      class="flex-container flex-centered box contact"
    >
      <h2>contact</h2>
    </div>
    <div v-else class="flex-container flex-centered box">
      <NuxtLink to="/contact" class="link">contact</NuxtLink>
    </div>
  </nav>
</template>

<script>
export default {
  computed: {
    currentPageName() {
      return this.$route.name
    },
  },
}
</script>

<style lang="scss" scoped>
.box {
  width: 150px;
  height: 150px;
  padding-left: 1em;
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
</style>
