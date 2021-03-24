<template>
  <nav>
    <nav-item-vue page-name="about"></nav-item-vue>
    <nav-item-vue page-name="projects"></nav-item-vue>
    <nav-item-vue page-name="contact"></nav-item-vue>
  </nav>
</template>

<script>
import NavItemVue from '~/components/NavItem.vue'

export default {
  components: { NavItemVue },
}
</script>

<style lang="scss" scoped></style>
