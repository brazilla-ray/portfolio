<template>
  <article>
    <section>
      <h3>
        <span class="terminal-prompt">$</span>&nbsp;<span class="command"
          >whoami</span
        >
      </h3>
      <p>hi! I'm a self-taught web developer who writes:</p>
      <dl>
        <dt>clean,</dt>
        <dt class="ml-1">semantic,</dt>
        <dt class="ml-2">accessible</dt>
        <dd class="ml-3">html</dd>
        <dd class="ml-3">css</dd>
        <dd class="ml-3">javascript</dd>
      </dl>
      <p>
        I live in the district of columbia where sometimes I
        <a href="https://williamwhitaker.art" class="link">make art</a>.
      </p>
    </section>
    <section>
      <h3>
        <span class="terminal-prompt">$</span>&nbsp;<span class="command"
          >history</span
        >
      </h3>
      <ul>
        <li>
          <span class="redacted">1997</span> BFA, painting, rhode island school
          of design
        </li>
        <li><span class="redacted">2001</span> art handler</li>
        <li>
          <span class="less-redacted">2007</span> started working
          <a href="https://nga.gov"><span class="link">here</span></a>
        </li>
        <li><span class="less-redacted">2009</span> built first website</li>
      </ul>
    </section>
    <section>
      <h3>
        <span class="terminal-prompt">$</span>&nbsp;<span class="command"
          >find</span
        >
      </h3>
      <ul>
        <li>
          <a href="https://twitter.com/w0whitaker" class="link">twitter</a>
        </li>
        <li>
          <a href="https://github.com/brazilla-ray" class="link">github</a>
        </li>
        <li>
          <a href="https://codepen.io/w0whitaker" class="link">codepen</a>
        </li>
      </ul>
    </section>
    <section>
      <h3>
        <span class="terminal-prompt">$</span>&nbsp;<span class="command"
          >more</span
        >
      </h3>
      <p>download <a href="/resume.pdf" download="" class="link">resume</a></p>
    </section>
  </article>
</template>

<style lang="scss" scoped>
section {
  margin-top: 1rem;
}

p,
ul,
li {
  padding: 0.5rem 0;
}

ul {
  list-style: none;
}
dd::before {
  content: '-> ';
  color: $green;
}

.terminal-prompt {
  color: magenta;
}

.command {
  color: $green;
}

.redacted {
  color: transparent;
  text-shadow: 0 0 5px #fffff0;
}

.less-redacted {
  color: transparent;
  text-shadow: 0 0 2.5px #fffff0;
}
</style>
