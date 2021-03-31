<template>
  <div>
    <img src="~/static/self.png" alt="self-portrait" class="inline-image" />
    <h3>
      <span class="terminal-prompt">$</span>&nbsp;<span class="command"
        >whoami</span
      >
    </h3>
    <p>
      Hi! I'm a self-taught web developer and an artist. I love learning new
      things and solving problems.
    </p>
    <p>
      I live in the District of Columbia, which is not a state, but definitely
      should be <a href="https://www.the51st.org/" class="link">one</a>.
    </p>
    <p>I like tacos, but my real passion is pizza.</p>
  </div>
</template>

<style lang="scss" scoped>
p {
  margin-top: 1em;
}
.inline-image {
  max-width: 150px;
  margin-top: -1em;
  margin-left: -1em;
  // margin: 0 1em 1em 0;
  float: left;
}

.terminal-prompt {
  color: magenta;
}

.command {
  color: greenyellow;
}
</style>
