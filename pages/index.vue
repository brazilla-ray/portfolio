<template>
  <div class="container">
    <div class="grid-container">
      <aside class="secondary pull-left">hello world! my name is...</aside>
      <div class="primary">
        <h1>William Whitaker</h1>
        <div class="links">
          <NuxtLink to="/about">about</NuxtLink>
          <NuxtLink to="/contact">contact</NuxtLink>
        </div>
      </div>
      <aside class="secondary pull-right">I am a...</aside>
      <div class="primary">
        <h2>developer</h2>
        <div class="links">
          <NuxtLink to="/projects">projects</NuxtLink>
        </div>
      </div>
      <aside class="secondary pull-left">and an...</aside>
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
export default {}
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
  justify-content: flex-end;
  flex: 1 1 100%;
  background: #00001f;
  align-items: center;
  align-content: center;
  flex-flow: row wrap;
  align-self: flex-end;
}

.links > a {
  color: #fffff0;
  height: 100%;
  padding-right: 3em;
}

.links > a:last-child {
  padding-right: 3px;
}

.secondary {
  background-color: #56b7eb;
  display: flex;
  justify-content: center;
  align-items: center;
  padding: 0 1.5em;
  height: 10vh;
}

.pull-left {
  grid-column: 1/7;
}

.pull-right {
  grid-column: 2/8;
}
</style>
