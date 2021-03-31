<template>
  <div class="normal light content-wrapper" :class="pageStyle">
    <slot></slot>
  </div>
</template>

<script>
export default {
  props: {
    pageStyle: {
      type: String,
      default: '',
    },
  },
}
</script>

<style lang="scss" scoped>
.content-wrapper {
  margin-right: -1em;
  padding: 1rem 1rem;
  border-left: 6px solid $near-black;
  border-bottom: 16px solid $near-black;
  height: 100%;
  overflow: hidden;
}

.about-content {
  background-color: $near-white-quarter-trans;
}

.projects-content {
  background-color: $blue-quarter-trans;
}

.contact-content {
  background-color: $yellow-quarter-trans;
}
</style>
