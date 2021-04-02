<template>
  <nav class="grid-container">
    <nav-item-vue page-name="about" class="row-1 col-span-10"></nav-item-vue>
    <div class="shadow-box about"></div>
    <nav-item-vue page-name="projects" class="row-2 col-span-10"></nav-item-vue>
    <div class="shadow-box projects"></div>
    <nav-item-vue page-name="contact" class="row-3 col-span-10"></nav-item-vue>
    <div class="shadow-box contact"></div>
  </nav>
</template>

<script>
import NavItemVue from '~/components/NavItem.vue'

export default {
  components: { NavItemVue },
}
</script>

<style lang="scss" scoped>
.shadow-box {
  opacity: 0.25;
  margin-right: -1em;
  grid-column: 11/-1;
}
</style>
