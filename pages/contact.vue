<template>
  <div class="container">
    <page-header-vue></page-header-vue>
    <h1 class="page-title">get in touch</h1>
    <form class="contact-form" @submit.prevent="sendEmail">
      <label class="form-input-label">Name</label>
      <input
        class="form-input"
        type="text"
        name="user_name"
        placeholder="name"
      />
      <label class="form-input-label">Email</label>
      <input
        class="form-input"
        type="email"
        name="user_email"
        placeholder="email"
      />
      <label class="form-input-label">Message</label>
      <textarea
        class="message-input"
        name="message"
        placeholder="type your message here"
      ></textarea>
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
  align-items: flex-start;
}

.form-input,
.message-input {
  width: 100%;
  border: none;
  height: 5vh;
  background-color: #00001f;
  color: #fffff0;
  border-bottom: 3px solid #fffff0;
  font-size: 1em;
  font-family: 'Alata', sans-serif;
}

.message-input {
  height: 35vh;
  border: none;
  background-color: #fffff0;
  color: #00001f;
}

.form-input-label {
  margin: 2em 0 1em;
  color: #56b7eb;
}
</style>
