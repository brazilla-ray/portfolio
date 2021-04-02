<template>
  <div class="grid-container">
    <NuxtLink
      :to="{ path: pageName }"
      :class="[pageName]"
      class="box flex-container flex-centered"
    >
      <h2 class="section-title">{{ pageName }}</h2>
    </NuxtLink>
  </div>
</template>

<script>
export default {
  props: {
    pageName: {
      type: String,
      default: '',
    },
  },
  data() {
    return {
      classList: ['flex-container', 'flex-centered', 'box'],
    }
  },
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
</style>
