<template>
  <div class="container">
    <aside class="secondary">hello world! my name is...</aside>
    <h1 class="primary">William Whitaker</h1>
    <div class="links">
      <a href="#">resume</a>
      <a href="#">contact</a>
    </div>
    <aside class="secondary">I am a...</aside>
    <h2 class="primary">developer</h2>
    <div class="links">
      <a href="#">projects</a>
      <a href="#">github</a>
      <a href="#">codepen</a>
    </div>
    <aside class="secondary">and an...</aside>
    <h2 class="primary">artist</h2>
    <div class="links">
      <a href="https://williamwhitaker.art">williamwhitaker.art</a>
    </div>
  </div>
</template>

<script>
export default {}
</script>

<style>
.container {
  margin: 0 auto;
  min-height: 100vh;
  display: grid;
  grid-template-columns: 35px auto 35px;
  grid-template-rows: auto;
  gap: 35px;
}

.primary {
  font-size: 2em;
  background-color: #fffff0;
  grid-column: 1/3;
  display: flex;
  justify-content: center;
  align-items: center;
}

.secondary {
  font-size: 1em;
  background-color: #56b7eb;
  grid-column: 2/4;
  display: flex;
  justify-content: center;
  align-items: center;
}

.links {
  display: none;
}
</style>
