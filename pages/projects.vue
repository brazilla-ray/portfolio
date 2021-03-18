<template>
  <div class="grid-container">
    <page-header-vue class="page-header"></page-header-vue>
    <div class="page-title">
      <h1>projects</h1>
    </div>
    <div class="content-wrapper">
      <article class="main-content">
        <section>
          <h2>art</h2>
          <br />
          <p>
            The first site I built for my artwork was pretty basic: HTML, CSS,
            and a little JavaScript. I went on to build sites with Drupal, Ruby
            on Rails, and WordPress. There may have been easier ways to go about
            it, but I've always liked making things from scratch.
          </p>
          <br />
          <figure>
            <a href="https://brazilla-ray.github.io/first-site/">
              <img
                src="~/static/first_site.png"
                class="screenshot"
                alt="My first website"
              />
            </a>
            <figcaption>
              <aside>My first site.</aside>
              <code>HTML, CSS, JavaScript</code>
            </figcaption>
          </figure>
          <figure>
            <img
              src="~/static/mrww_v1.png"
              class="screenshot"
              alt="mrwilliamwhitaker.com screenshot"
            />
            <figcaption>
              <aside>mrwilliamwhitaker.com, c.2011</aside>
              <code>Drupal</code>
            </figcaption>
          </figure>
          <figure>
            <img
              src="~/static/mrww_v2.png"
              class="screenshot"
              alt="mrwilliamwhitaker.com screenshot"
            />
            <figcaption>
              <aside>c.2013</aside>
              <code>Drupal</code>
            </figcaption>
          </figure>
          <figure>
            <img
              src="~/static/mrww_v3.png"
              class="screenshot"
              alt="mrwilliamwhitaker.com screenshot"
            />
            <figcaption>
              <aside>c.2015</aside>
              <code>Ruby on Rails</code>
            </figcaption>
          </figure>
          <br />
          <p>
            Last summer, I switched my domain to
            <a href="https://williamwhitaker.art">williamwhitaker.art</a>
            and coded my first WordPress
            <a href="https://github.com/brazilla-ray/ww-theme">theme</a>, based
            on <a href="https://underscores.me/">_s</a>, as well as my first
            <a href="https://github.com/brazilla-ray/ww-plugin">plugin.</a>
          </p>
          <br />
          <p>
            I'm currently working on a
            <a href="https://github.com/brazilla-ray/wwa-client">version</a>
            that uses WordPress as a headless CMS, with a Nuxt app as the
            frontend. You can preview it
            <a href="https://pensive-aryabhata-8caa68.netlify.app/">here</a>.
          </p>
        </section>
        <section>
          <br />
          <h2>other things</h2>
          <br />
          <p>
            When I got married, I built the website for our wedding.
            <a href="https://brazilla-ray.github.io/wedding-site/">It</a>
            handled the RSVPs and menu choice of the guests.
          </p>
          <p>
            You can check out some of the things I've made on
            <a href="https://codepen.io/w0whitaker">CodePen</a>, including
            <a href="https://codepen.io/collection/DKwbKa">this</a> collection
            that was a picked pen a while back.
          </p>
          <br />
          <figure>
            <img src="~/static/codePen.png" alt="CodePen" class="screenshot" />
            <aside>Exciting!</aside>
          </figure>
        </section>
      </article>
    </div>
  </div>
</template>

<script>
import PageHeaderVue from '~/components/PageHeader.vue'

export default {
  components: { PageHeaderVue },
}
</script>

<style lang="scss" scoped>
.grid-container::after {
  background-color: $blue;
  grid-column: 7/12;
}

article > p {
  margin-top: 35px;
}

article > p > a {
  color: #56b7eb;
}

.screenshot {
  width: 250px;
  padding: 3px;
}
</style>
