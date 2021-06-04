<template>
  <article>
    <section>
      <h3>mrwilliamwhitaker.com</h3>
      <ul class="mt-1">
        <li>
          <p>
            the
            <a href="https://brazilla-ray.github.io/first-site/" class="link"
              >first</a
            >
            website I made was just:
          </p>
          <ul class="ml-1">
            <li>html</li>
            <li>&amp; css</li>
          </ul>
        </li>
        <li class="mt-1">
          <p>I've since made versions of it using:</p>
          <ul class="ml-1">
            <li>drupal</li>
            <li>ruby on rails</li>
            <li>&amp; wordpress</li>
          </ul>
        </li>
      </ul>
    </section>
    <section class="mt-1">
      <h3>williamwhitaker.art</h3>
      <ul class="mt-1">
        <li class="mt-1">
          <p>
            my
            <a href="https://williamwhitaker.art" class="link">current</a> site:
          </p>
          <ul class="ml-1">
            <li>wordpress</li>
            <li>custom theme</li>
          </ul>
        </li>
        <li class="mt-1">
          <p>
            in
            <a href="https://pensive-aryabhata-8caa68.netlify.app/" class="link"
              >development</a
            >:
          </p>
          <ul class="ml-1">
            <li>headless cms (wordpress)</li>
            <li>nuxt/vue</li>
            <li>netlify</li>
          </ul>
        </li>
      </ul>
    </section>
    <section class="mt-1">
      <h3>other projects</h3>
      <h4>
        <a href="https://brazilla-ray.github.io/pieton/" class="link"
          >pi&eacute;ton</a
        >
      </h4>
      <p class="long-line">
        a CSS color system that's meant to be accessible despite the fancy name.
      </p>
      <h4>
        <a href="https://brazilla-ray-pomodoro.netlify.app/" class="link"
          >pomodoro timer</a
        >
      </h4>
      <p class="long-line">
        a simple pomodoro timer that I made complicated by using Vue/Vuex/Nuxt.
      </p>
      <div class="flex-container">
        <h5>also available:</h5>
        <ul class="ml-1">
          <li>
            <a href="https://github.com/brazilla-ray" class="link">github</a>
          </li>
          <li>
            <a href="https://codepen.io/w0whitaker" class="link"
              >&amp; codepen</a
            >
          </li>
        </ul>
      </div>
    </section>
  </article>
</template>

<script>
export default {}
</script>

<style lang="scss" scoped>
h3 {
  font-size: 1em;
  color: $green;
}

ul {
  list-style: none;
  padding: 0;
  margin: 0;
}

li,
p,
h4,
h5 {
  margin-top: 1.25rem;
}

h5 {
  padding-top: 1.75rem;
}

p {
  line-height: 2;
}

img {
  max-width: 150px;
}

.long-line {
  max-width: 33.3%;
}

.flex-container {
  display: flex;
}
</style>
