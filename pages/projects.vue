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
          <p>
            The first site I built for my artwork was pretty basic: HTML, CSS,
            and a little JavaScript. I went on to build sites with Drupal, Ruby
            on Rails, and WordPress. There may have been easier ways to go about
            it, but I've always liked making things from scratch.
          </p>
          <figure>
            <a href="https://brazilla-ray.github.io/first-site/">
              <img
                src="~/static/first_site.jpg"
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
              src="~/static/mrww_v1.jpg"
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
              src="~/static/mrww_v2.jpg"
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
              src="~/static/mrww_v3.jpg"
              class="screenshot"
              alt="mrwilliamwhitaker.com screenshot"
            />
            <figcaption>
              <aside>c.2015</aside>
              <code>Ruby on Rails</code>
            </figcaption>
          </figure>
          <p>
            Last summer, I switched my domain to
            <a href="https://williamwhitaker.art">williamwhitaker.art</a>
            and coded my first WordPress
            <a href="https://github.com/brazilla-ray/ww-theme">theme</a>, based
            on <a href="https://underscores.me/">_s</a>, as well as my first
            <a href="https://github.com/brazilla-ray/ww-plugin">plugin.</a>
          </p>
          <figure>
            <img
              src="~/static/current_site.jpg"
              class="screenshot"
              alt="mrwilliamwhitaker.com screenshot"
            />
            <figcaption>
              <aside>c.2015</aside>
              <code>Ruby on Rails</code>
            </figcaption>
          </figure>
          <p>
            I'm currently working on a
            <a href="https://github.com/brazilla-ray/wwa-client">version</a>
            that uses WordPress as a headless CMS, with a Nuxt app as the
            frontend. You can preview it
            <a href="https://pensive-aryabhata-8caa68.netlify.app/">here</a>.
          </p>
        </section>
        <section>
          <h2>other things</h2>
          <p>
            When I got married, I built the website for our wedding.
            <a href="https://brazilla-ray.github.io/wedding-site/">It</a>
            handled the RSVPs and menu choice of the guests.
          </p>
          <p>
            You can check out some of the things I've made on
            <a href="https://codepen.io/w0whitaker">CodePen</a>, including
            <a href="https://codepen.io/collection/DKwbKa">this</a> collection
            that was featured a while back.
          </p>
          <figure>
            <img src="~/static/codePen.png" alt="CodePen" class="screenshot" />
          </figure>
          <p>
            I'm also on <a href="https://github.com/brazilla-ray">github</a>.
          </p>
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

section {
  margin-bottom: 2em;
}

section > p {
  margin-top: 2em;
  line-height: 1.5;
}

figure {
  font-size: 0.75em;
  display: flex;
  flex-flow: column;
  align-items: center;
  margin-top: 4em;
}

figure img {
  align-self: center;
  border: 2px solid $near-white-quarter-trans;
  border-radius: 5%;
}

figcaption {
  margin-top: 1em;
}

figcaption > aside {
  font-style: italic;
}

.screenshot {
  max-width: 250px;
  height: auto;
}

@media screen and (min-width: 768px) {
  article {
    display: flex;
    flex-flow: row wrap;
    justify-content: space-between;
  }

  section {
    display: flex;
    flex-flow: row wrap;
    justify-content: space-between;
  }

  figure {
    flex: 0 0 43%;
  }
}

@media screen and (min-width: 1024px) {
  section > h2 {
    flex: 1 0 90%;
  }

  section > p {
    flex: 0 1 25%;
    margin-top: 3em;
  }

  figure {
    flex: 0 0 33%;
    margin-top: 3em;
  }

  figure img {
    align-self: flex-start;
  }
}
</style>
