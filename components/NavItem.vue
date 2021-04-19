<template>
  <NuxtLink
    :to="{ path: pageName }"
    :class="[
      currentPageName === 'index' || currentPageName === pageName
        ? pageName
        : '',
    ]"
    class="grid-container_box"
  >
    <h2
      v-if="currentPageName === 'index' || currentPageName === pageName"
      class="section-title col-2 row-4-span-2"
    >
      {{ pageName }}
    </h2>
    <span v-else class="link col-2 row-4-span-2">{{ pageName }}</span>
  </NuxtLink>
</template>

<script>
export default {
  props: {
    pageName: {
      type: String,
      default: '',
    },
  },
  computed: {
    currentPageName() {
      return this.$route.name
    },
  },
}
</script>

<style lang="scss" scoped></style>
