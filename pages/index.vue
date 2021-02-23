<template>
  <div class="container">
    <div class="grid-container">
      <aside class="secondary">hello world! my name is...</aside>
      <div class="primary">
        <h1>William Whitaker</h1>
        <div class="links">
          <NuxtLink to="/about">about</NuxtLink>
          <NuxtLink to="/contact">contact</NuxtLink>
        </div>
      </div>
      <aside class="secondary">I am a...</aside>
      <div class="primary">
        <h2>developer</h2>
        <div class="links">
          <NuxtLink to="/projects">projects</NuxtLink>
        </div>
      </div>
      <aside class="secondary">and an...</aside>
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
  grid-template-columns: 35px 50%;
  grid-template-rows: auto;
  gap: 35px;
}

.primary {
  background-color: #fffff0;
  grid-column: 2/4;
  display: flex;
  justify-content: flex-start;
  align-items: flex-end;
  flex-flow: row wrap;
}

.primary > h1,
.primary > h2 {
  font-size: 2em;
  font-weight: normal;
  padding-left: 0.25em;
}

.links {
  display: flex;
  justify-content: flex-start;
  flex: 1 1 100%;
  background: #00001f;
  align-items: center;
  align-content: center;
  flex-flow: row wrap;
  align-self: flex-end;
}

.links > a {
  color: #fffff0;
  padding: 1em 3em 0 0.5em;
  height: 100%;
}
.secondary {
  background-color: #56b7eb;
  grid-column: 1/3;
  display: flex;
  justify-content: flex-end;
  align-items: center;
  padding-right: 0.5em;
}

.slide-fade-enter-active {
  transition: all 0.3s ease;
}
.slide-fade-leave-active {
  transition: all 0.8s cubic-bezier(1, 0.5, 0.8, 1);
}
.slide-fade-enter, .slide-fade-leave-to
/* .slide-fade-leave-active below version 2.1.8 */ {
  transform: translateX(10px);
  opacity: 0;
}
</style>
