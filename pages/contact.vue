<template>
  <div class="grid-container">
    <div class="indented">
      <header-vue tag-line="loves getting mail"></header-vue>
    </div>
    <div class="full-width row-2">
      <main-nav-vue></main-nav-vue>
    </div>
    <div class="content row-2">
      <main-content-vue page-style="contact-content">
        <contact-form-vue></contact-form-vue>
      </main-content-vue>
    </div>
  </div>
</template>

<script>
import HeaderVue from '~/components/Header.vue'
import MainNavVue from '~/components/MainNav.vue'
import MainContentVue from '~/components/MainContent.vue'
import ContactFormVue from '~/components/ContactForm.vue'

export default {
  components: {
    HeaderVue,
    MainNavVue,
    MainContentVue,
    ContactFormVue,
  },
}
</script>

<style lang="scss" scoped></style>
