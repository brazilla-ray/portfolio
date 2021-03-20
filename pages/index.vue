<template>
  <div class="content">
    <header class="flex-container">
      <header-vue></header-vue>
      <sub-header-vue></sub-header-vue>
    </header>
  </div>
</template>

<script>
import HeaderVue from '~/components/Header.vue'
import SubHeaderVue from '~/components/SubHeader.vue'
export default {
  components: {
    HeaderVue,
    SubHeaderVue,
  },
}
</script>

<style lang="scss" scoped>
header {
  margin: 1em 1em 0;
}
</style>
