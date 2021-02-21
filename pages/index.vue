<template>
  <div class="container">
    <aside class="secondary">hello world! my name is...</aside>
    <h1 class="primary">
      <button @click="show = !show">William Whitaker</button>
    </h1>
    <transition name="slide-fade">
      <div v-if="show" class="links">
        <a href="#">resume</a>
        <a href="#">contact</a>
      </div>
    </transition>
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
export default {
  data() {
    return {
      show: false,
    }
  },
}
</script>

<style>
.container {
  margin: 35px auto 0;
  min-height: 100vh;
  display: grid;
  grid-template-columns: 35px auto 35px;
  grid-template-rows: auto;
  gap: 35px;
}

.primary {
  font-size: 2em;
  background-color: #fffff0;
  grid-column: 2/4;
  display: flex;
  justify-content: center;
  align-items: center;
}

.primary > button {
  border: none;
  background-color: transparent;
  font-family: 'Alata', sans-serif;
  font-size: 1.25em;
}

.secondary {
  font-size: 1em;
  background-color: #56b7eb;
  grid-column: 1/3;
  display: flex;
  justify-content: center;
  align-items: center;
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

.links {
  grid-column: 2/4;
  display: flex;
  justify-content: space-around;
  align-items: center;
}
</style>
