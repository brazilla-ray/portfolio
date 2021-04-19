<template>
  <form class="contact-form" @submit.prevent="sendEmail">
    <label class="form-input-label">Name</label>
    <input class="form-input" type="text" name="user_name" placeholder="name" />
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
</template>

<script>
export default {}
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
  background-color: transparent;
  color: $near-white;
  border-bottom: 3px solid $near-white;
  font-size: 1em;
  font-family: 'Alata', sans-serif;
}

.form-input-label {
  margin: 2em 0 1em;
  color: $near-white;
}

.message-input {
  height: 35vh;
  border: none;
  background-color: $near-white;
  color: $near-black;
}

.message-submit {
  border: 3px solid $near-white;
  font-size: 2em;
  color: $near-white;
  background-color: transparent;
  font-family: 'Alata', sans-serif;
  margin-top: 17.5px;
  border-radius: 10%;
}
</style>
