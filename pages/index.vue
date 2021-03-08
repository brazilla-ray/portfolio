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
  grid-template-columns: 50vw 50vw;
  grid-template-rows: 15vh 25vh 25vh 45vh;
}

.grid-container::after {
  content: '';
  background-color: $green;
  grid-column: 1;
  grid-row: 4;
}

.grid-boxes {
  height: auto;
}

.with-text {
  display: flex;
  flex-flow: row nowrap;
  text-decoration: none;
}

.with-text h1,
.with-text h2 {
  font-size: 2rem;
  padding: 0.5em;
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
}

.title::before {
  content: '';
  width: 40%;
  display: block;
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

.contact::before {
  content: '';
  width: 40%;
  display: block;
}

.box-7 {
  background-color: $green;
  transform: skewX(15deg);
  transform-origin: top;
  grid-column: 1;
  grid-row: 4;
}
</style>
