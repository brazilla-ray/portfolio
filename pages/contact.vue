<template>
  <div class="container">
    <page-header-vue></page-header-vue>
    <div class="content-wrapper">
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
        <input class="message-submit" type="submit" value="Send" />
      </form>
    </div>
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

<style lang="scss" scoped>
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
