<template>
  <div class="grid-container">
    <header class="flex-container content">
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

<style lang="scss" scoped></style>
