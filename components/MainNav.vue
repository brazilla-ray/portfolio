<template>
  <nav class="mt-1">
    <div
      v-if="currentPageName === 'about' || currentPageName === 'index'"
      class="flex-container flex-centered box about section-title mt-1"
    >
      <NuxtLink to="/about">
        <h2>about</h2>
      </NuxtLink>
    </div>
    <div v-else class="flex-container flex-centered box">
      <NuxtLink to="/about" class="link">about</NuxtLink>
    </div>
    <div
      v-if="currentPageName === 'projects' || currentPageName === 'index'"
      class="flex-container flex-centered box projects section-title mt-1"
    >
      <NuxtLink to="/projects">
        <h2>projects</h2>
      </NuxtLink>
    </div>
    <div v-else class="flex-container flex-centered box">
      <NuxtLink to="/projects" class="link">projects</NuxtLink>
    </div>
    <div
      v-if="currentPageName === 'contact' || currentPageName === 'index'"
      class="flex-container flex-centered box contact section-title mt-1"
    >
      <NuxtLink to="/contact">
        <h2>contact</h2>
      </NuxtLink>
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
</style>
