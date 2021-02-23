<template>
  <div>
    <page-header-vue></page-header-vue>
    <div>
      <p>some content</p>
    </div>
  </div>
</template>

<script>
import PageHeaderVue from '~/components/PageHeader.vue'
export default {
  components: { PageHeaderVue },
}
</script>

<style scoped>
p {
  color: #fffff0;
}
</style>
