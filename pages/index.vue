<template>
  <div class="container">
    <page-header-vue></page-header-vue>
    <div class="grid-container">
      <aside class="secondary pull-left">
        <p>hello world! my name is...</p>
      </aside>
      <div class="primary">
        <h1>William Whitaker</h1>
        <div class="links">
          <NuxtLink to="/about">about</NuxtLink>
          <NuxtLink to="/contact">contact</NuxtLink>
        </div>
      </div>
      <aside class="secondary pull-right"><p>I am a...</p></aside>
      <div class="primary">
        <h2>developer</h2>
        <div class="links">
          <NuxtLink to="/projects">projects</NuxtLink>
        </div>
      </div>
      <aside class="secondary pull-left"><p>and an...</p></aside>
      <div class="primary">
        <h2>artist</h2>
        <div class="links">
          <a href="https://williamwhitaker.art">williamwhitaker.art</a>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
import PageHeaderVue from '~/components/PageHeader.vue'

export default {
  components: { PageHeaderVue },
}
</script>

<style scoped>
.grid-container {
  display: grid;
  grid-template-columns: auto;
  grid-template-rows: auto;
  gap: 35px;
}

.primary {
  background-color: #fffff0;
  grid-column: 1/8;
  display: flex;
  justify-content: center;
  align-items: flex-end;
  flex-flow: row wrap;
  height: 12vh;
}

.primary > h1,
.primary > h2 {
  font-size: 2em;
  font-weight: normal;
  padding: 0 3px 0;
}

.links {
  display: flex;
  justify-content: center;
  flex: 1 1 100%;
  background: #00001f;
  align-items: center;
  align-content: center;
  flex-flow: row wrap;
  align-self: flex-end;
  font-size: 1.75em;
  margin: 0;
}

.links > a {
  color: #fffff0;
  padding-right: 3em;
}

.links > a:last-child {
  padding-right: 3px;
}

.secondary {
  background-color: #56b7eb;
  font-size: 1.5em;
  display: flex;
  justify-content: center;
  align-items: center;
  padding: 1.5em;
  height: 10vh;
}

.pull-left {
  grid-column: 1/8;
  margin-left: -35px;
}

.pull-right {
  grid-column: 1/8;
  margin-right: -35px;
}

page-header-vue {
  display: none;
}

@media screen and (min-width: 1024px) {
  /* TODO: improve on this. maybe conditional classes 
  *  based on window size. */
  .grid-container {
    display: flex;
    flex-flow: row nowrap;
    justify-content: center;
  }

  .primary,
  .secondary {
    height: 50vh;
    width: calc(100vw / 3);
  }

  .primary {
    margin: calc(75vh / 2) 0 0 -35px;
    justify-content: center;
    align-items: center;
  }

  .primary > h1,
  .primary > h2 {
    font-size: 2em;
    font-weight: normal;
    padding: 0 1em 0;
  }
  /* 
  .primary:last-child {
    width: 25%;
  } */

  .secondary {
    margin: calc(75vh / 3) 0 0 -35px;
    justify-content: flex-start;
  }

  .secondary > p {
    padding-left: 1em;
  }

  .links {
    display: none;
  }
}
</style>
