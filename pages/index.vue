<template>
  <div class="container">
    <div class="grid-container">
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
    </div>
  </div>
</template>

<script></script>

<style lang="scss" scoped>
.grid-container {
  display: grid;
  grid-template-columns: repeat(4, 25vw);
  grid-template-rows: 15vh 25vh 25vh 45vh;
}

.grid-container::before {
  content: '';
  background-color: $blue-trans;
  grid-column: 3/5;
  grid-row: 1;
  transform: skewX(45deg);
  transform-origin: bottom;
}

.grid-container::after {
  content: '';
  background-color: $blue-trans;
  transform: skewX(15deg) translateX(-33.3%);
  transform-origin: top;
  grid-column: 1/4;
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

.title {
  color: $near-white;
  background-color: $warm-gray;
  grid-column: 1/3;
  grid-row: 2;
}

.title h1 {
  align-self: flex-end;
}

.title::before {
  content: '';
  width: 40%;
  display: block;
}

.title::after {
  content: '';
  display: block;
  width: 50%;
  height: 15vh;
  position: absolute;
  top: 0;
  left: 0;
  transform: skewX(45deg);
  transform-origin: bottom;
  background-color: $warm-gray-trans;
}

.projects {
  background-color: $blue;
  color: rgb(0, 0, 31);
  grid-column: 3/5;
  grid-row: 2;
}

.about {
  background-color: $near-white;
  color: rgb(0, 0, 31);
  grid-column: 1/3;
  grid-row: 3;
}

.about h2 {
  align-self: flex-end;
}

.contact {
  background-color: $yellow;
  color: rgb(0, 0, 31);
  grid-column: 3/5;
  grid-row: 3;
}

.contact::before {
  content: '';
  width: 40%;
  display: block;
}

@media screen and (min-width: 568px) {
  .grid-container {
    grid-template-rows: 15vh 35vh 35vh 20vh;
  }

  .grid-container::before {
    grid-column: 3/4;
    grid-row: 4;
    transform: skewX(15deg);
    transform-origin: top;
  }

  .grid-container::after {
    grid-column: 4;
    grid-row: 1/3;
    transform: skewX(340deg);
    transform-origin: bottom;
  }

  .title {
    grid-column: 1/3;
    grid-row: 2;
  }

  .projects {
    grid-column: 3;
    grid-row: 3;
  }

  .about {
    grid-column: 2;
    grid-row: 3;
  }

  .contact {
    grid-column: 4;
    grid-row: 3;
  }
}

@media screen and (min-width: 768px) {
  .grid-container {
    grid-template-columns: repeat(8, 12.5vw);
    grid-template-rows: repeat(8, 12.5vh);
    overflow: hidden;
  }

  .grid-container::before {
    grid-column: 7/9;
    grid-row: 1/3;
    transform: skewY(22.3deg);
    transform-origin: left top;
    background-color: $warm-gray-trans;
  }

  .grid-container::after {
    grid-column: 1/5;
    grid-row: 5/9;
    transform: skewY(-58deg);
    transform-origin: top right;
    background-color: $blue-dark;
  }

  .title {
    grid-column: 1/7;
    grid-row: 1/3;
  }

  .title::before,
  .title::after {
    display: none;
  }

  .about {
    grid-column: 5/7;
    grid-row: 3/5;
  }

  .projects {
    grid-column: 5/7;
    grid-row: 5/7;
  }

  .contact {
    grid-column: 4/8;
    grid-row: 7/9;
    border-left: 12em solid $blue-dark;
  }

  .with-text h1,
  .with-text h2 {
    font-size: 2.5em;
  }

  .with-text {
    justify-content: flex-end;
    align-items: center;
  }
}
</style>
