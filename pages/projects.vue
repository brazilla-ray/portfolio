<template>
  <div class="container">
    <page-header-vue></page-header-vue>
    <h1 class="page-title">projects</h1>
    <section>
      <h2 class="section-title">my website over the years...</h2>
      <article class="section-content">
        <p>
          I've made several websites to showcase my artwork. This first was just
          a simple, static HTML site. There was a tiny bit of Javascript in
          there too.
        </p>
        <a href="https://brazilla-ray.github.io/first-site/">
          <img
            class="screenshot"
            src="~/static/JPEG/first_site.jpg"
            alt="my first website"
          />
        </a>
        <p>
          I quickly realized two things: first, I loved doing this, and second,
          that I would have to update things by hand. Which led me to Drupal. I
          coded this one during a blizzard.
        </p>
        <img
          class="screenshot"
          src="~/static/JPEG/mrww_v1.jpg"
          alt="drupal site version 1"
        />
        <p>
          This is another version, where I tried my hand at building a theme
          from scratch.
        </p>
        <img
          class="screenshot"
          src="~/static/JPEG/mrww_v2.jpg"
          alt="drupal site 2013"
        />
        <p>At one point, I decided to learn Ruby on Rails.</p>
        <img
          class="screenshot"
          src="~/static/JPEG/mrww_v3.jpg"
          alt="rails site 2014"
        />
        <p>
          This is the current version of my site. It's a WordPress site, with a
          custom theme I coded.
        </p>
        <a href="https://williamwhitaker.art">
          <img
            class="screenshot"
            src="~/static/JPEG/current_site.jpg"
            alt="current site"
          />
        </a>
        <p>
          I'm currently working on a
          <a href="https://pensive-aryabhata-8caa68.netlify.app/">version</a>
          that uses WordPress as a headless CMS, with a Nuxt app on the
          frontend. It should be finished soon!
        </p>
      </article>
    </section>
    <section>
      <h2 class="section-title">some other projects...</h2>
      <article class="section-content">
        <p>
          I made an Angular
          <a href="https://brazilla-ray.github.io/sarApp/">app</a> for my
          sister, who's a published
          <a
            href="https://www.amazon.com/What-Comes-Dreams-Sarah-Robinson/dp/1480873233/ref=sr_1_1?dchild=1&keywords=what+comes+of+dreams+sarah+robinson&qid=1614222591&sr=8-1"
            >author!</a
          >
        </p>
        <img
          class="screenshot"
          src="~/static/JPEG/sar_sketch.jpg"
          alt="sarApp sketch"
        />
        <p>I really need to get back to work on that one.</p>
        <p>
          Last but not least is the
          <a href="https://brazilla-ray.github.io/wedding-site/">site</a> I made
          for my wedding in 2016. I built it using Yeoman and Gulp. I had a lot
          of trouble with getting the form working, but a friend helped me out.
        </p>
        <img
          class="screenshot"
          src="~/static/JPEG/wedding_site.jpg"
          alt="wedding site"
        />
      </article>
    </section>
  </div>
</template>

<script>
import PageHeaderVue from '~/components/PageHeader.vue'

export default {
  components: {
    PageHeaderVue,
  },
}
</script>

<style scoped>
article > p {
  margin-top: 35px;
}

article > p > a {
  color: #56b7eb;
}

.screenshot {
  width: 250px;
  margin-top: 35px;
  border-radius: 5%;
  border: 3px solid #11111a;
  padding: 3px;
}
</style>
