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
  grid-template-columns: repeat(8, 12.5vw);
  grid-template-rows: repeat(8, 12.5vh);
  overflow: hidden;
}

.grid-container::before {
  content: '';
  background-color: $warm-gray-trans;
  grid-column: 1/9;
  grid-row: 1;
  transform: skewX(315deg);
  transform-origin: bottom;
}

.grid-boxes {
  height: auto;
}

.with-text {
  display: flex;
  flex-flow: row nowrap;
  justify-content: flex-end;
  align-items: center;
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
  grid-column: 1/9;
  grid-row: 2/4;
}

.title h1 {
  align-self: flex-end;
}

.projects {
  background-color: $blue;
  color: rgb(0, 0, 31);
  grid-column: 5/9;
  grid-row: 4/6;
}

.about {
  background-color: $near-white;
  color: rgb(0, 0, 31);
  grid-column: 1/5;
  grid-row: 4/6;
}

.about h2 {
  align-self: flex-end;
}

.contact {
  background-color: $yellow;
  color: rgb(0, 0, 31);
  grid-column: 5/9;
  grid-row: 6/8;
}

@media screen and (min-width: 568px) {
  .title {
    grid-row: 2/5;
  }

  .projects,
  .about,
  .contact {
    grid-row: 5/9;
  }

  .projects {
    grid-column: 5/7;
  }

  .contact {
    grid-column: 7/9;
  }

  .about {
    grid-column: 3/5;
  }
}

@media screen and (min-width: 768px) {
  .title {
    grid-column: 1/9;
    grid-row: 2/4;
  }

  .about,
  .projects {
    grid-row: 4/6;
  }

  .about {
    grid-column: 3/6;
  }

  .projects {
    grid-column: 6/9;
  }

  .contact {
    grid-column: 6/9;
    grid-row: 6/8;
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

@media screen and (min-width: 1024px) {
  .grid-container::before {
    grid-column: 2/7;
  }

  .title::before {
    content: '';
    display: block;
    position: absolute;
    top: 0;
    right: 12.5vw;
    height: 12.5vh;
    width: 12.5vw;
    background-color: $warm-gray-dark;
  }

  .title {
    grid-column: 2/8;
  }

  .about {
    grid-column: 4/6;
  }

  .about,
  .projects {
    grid-row: 4/7;
  }

  .projects {
    grid-column: 6/8;
  }

  .contact {
    grid-column: 4/8;
    grid-row: 7/9;
  }
}
</style>
