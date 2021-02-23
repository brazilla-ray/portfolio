<template>
  <div class="container">
    <page-header-vue></page-header-vue>
    <h1 class="page-title">get in touch</h1>
    <form class="contact-form" @submit.prevent="sendEmail">
      <label class="form-input-label">Name</label>
      <input class="form-input" type="text" name="user_name" />
      <label class="form-input-label">Email</label>
      <input class="form-input" type="email" name="user_email" />
      <label class="form-input-label">Message</label>
      <textarea class="form-input" name="message"></textarea>
      <input type="submit" value="Send" />
    </form>
  </div>
</template>

<script>
import emailjs from 'emailjs-com'
import PageHeaderVue from '~/components/PageHeader.vue'

export default {
  components: {
    PageHeaderVue,
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

<style scoped>
.contact-form {
  display: flex;
  flex-flow: column;
  align-items: center;
}

.form-input {
  width: 75%;
  border: none;
  height: 3em;
}

.form-input-label {
  margin: 2em 0 1em;
  color: #56b7eb;
}
</style>
