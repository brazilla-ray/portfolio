<template>
  <div class="normal light content-wrapper" :class="pageStyle">
    <p>
      Lorem ipsum dolor sit amet consectetur adipisicing elit. Atque ducimus
      praesentium totam consequuntur molestias, nemo molestiae a asperiores eius
      quam earum amet incidunt sed explicabo, iste ex temporibus dolorum sint!
    </p>
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
  padding: 1rem 2rem;
  border-left: 6px solid $near-black;
  border-bottom: 16px solid $near-black;
  height: 100%;
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
