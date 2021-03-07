<template>
  <div class="container">
    <div class="grid-container">
      <div class="grid-boxes box-1"></div>
      <div class="grid-boxes box-2"></div>
      <NuxtLink to="/" class="grid-boxes with-text title">
        <h1>William Whitaker</h1>
      </NuxtLink>
      <NuxtLink to="/projects" class="grid-boxes with-text projects">
        <h2>projects</h2>
      </NuxtLink>
      <NuxtLink to="/about" class="grid-boxes with-text about">
        <h2>about</h2>
      </NuxtLink>
      <NuxtLink to="/contact" class="grid-boxes with-text contact">
        <h2>contact</h2>
      </NuxtLink>
      <div class="grid-boxes box-7"></div>
      <div class="grid-boxes box-8"></div>
    </div>
  </div>
</template>

<script></script>

<style lang="scss" scoped>
.grid-container {
  display: grid;
  grid-template-columns: 50% 50%;
  grid-template-rows: 15vh 25vh 25vh 85vh;
}

.grid-boxes {
  height: auto;
  width: 11.719em;
}

.with-text {
  display: flex;
  flex-flow: row wrap;
  text-decoration: none;
}

.with-text h1,
.with-text h2 {
  font-size: 2em;
}

.box-1 {
  background-color: $warm-gray-trans;
  transform: skewX(45deg);
  transform-origin: bottom;
}

.box-2 {
  background-color: $blue-trans;
  transform: skewX(45deg);
  transform-origin: bottom;
}

.title {
  color: $near-white;
  background-color: $warm-gray;
}

.title h1 {
  align-self: flex-end;
  padding-left: 1.5em;
}

.projects {
  background-color: $blue;
  color: rgb(0, 0, 31);
}

.about {
  background-color: $near-white;
  color: rgb(0, 0, 31);
}

.about h2 {
  align-self: flex-end;
}

.contact {
  background-color: $yellow;
  color: rgb(0, 0, 31);
}

.contact h2 {
  padding-left: 2em;
}

.box-7 {
  background-color: $blue-trans;
}

.box-8 {
  background: linear-gradient(64.5deg, $blue-trans 59%, transparent 0) top left;
}
</style>
