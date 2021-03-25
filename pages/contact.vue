<template>
  <div class="grid-container">
    <div class="indented">
      <header-vue site-title="ww"></header-vue>
    </div>
    <div class="full-width">
      <main-nav-vue></main-nav-vue>
    </div>
    <div class="content behind">
      <main-content-vue
        page-style="contact-content"
        class="mt-1"
      ></main-content-vue>
    </div>
  </div>
</template>

<script>
import emailjs from 'emailjs-com'
import HeaderVue from '~/components/Header.vue'
import MainNavVue from '~/components/MainNav.vue'
import MainContentVue from '~/components/MainContent.vue'

export default {
  components: {
    HeaderVue,
    MainNavVue,
    MainContentVue,
  },
  methods: {
    sendEmail: (e) => {
      emailjs
        .sendForm(
          'contact_service',
          'contact_form',
          e.target,
          'user_OPqabWgigbbWbuhIrLAhj'
        )
        .then(
          (result) => {
            console.log('SUCCESS!', result.status, result.text)
          },
          (error) => {
            console.log('FAILED...', error)
          }
        )
    },
  },
}
</script>

<style lang="scss" scoped>
.grid-container::after {
  background-color: $yellow;
  grid-column: 10/17;
}

.contact-form {
  display: flex;
  flex-flow: column;
  align-items: flex-start;
}

.form-input,
.message-input {
  width: 100%;
  border: none;
  height: 5vh;
  background-color: $near-black;
  color: $near-white;
  border-bottom: 3px solid $near-white;
  font-size: 1em;
  font-family: 'Alata', sans-serif;
}

.form-input-label {
  margin: 2em 0 1em;
  color: #56b7eb;
}

.message-input {
  height: 35vh;
  border: none;
  background-color: $near-white;
  color: $near-black;
}

.message-submit {
  border: 3px solid #56b7eb;
  font-size: 2em;
  color: #56b7eb;
  background-color: $near-black;
  font-family: 'Alata', sans-serif;
  margin-top: 17.5px;
  border-radius: 10%;
}
</style>
