<template>
  <div>
    <div
      v-if="currentPageName === pageName || currentPageName === 'index'"
      :class="[pageName, classList]"
    >
      <NuxtLink :to="{ path: pageName }">
        <h2 class="section-title">{{ pageName }}</h2>
      </NuxtLink>
    </div>
    <div v-else :class="classList">
      <NuxtLink :to="{ path: pageName }" class="link">{{ pageName }}</NuxtLink>
    </div>
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
      classList: ['flex-container', 'flex-centered', 'box', 'mt-1'],
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
