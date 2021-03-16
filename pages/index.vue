<template>
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
    <div class="grid-boxes message">
      <h3>work in progress:</h3>
      <p>
        I have decided to publish this site 'as-is', even though it's not
        'ready'.
      </p>
    </div>
  </div>
</template>

<script></script>

<style lang="scss" scoped>
.grid-container::before {
  content: '';
  background-color: $warm-gray-dark;
  grid-column: 1/17;
  grid-row: 1/3;
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
  grid-column: 1/17;
  grid-row: 3/8;
}

.title h1 {
  align-self: flex-end;
}

.projects {
  background-color: $blue;
  color: rgb(0, 0, 31);
  grid-column: 10/17;
  grid-row: 8/12;
}

.about {
  background-color: $near-white;
  color: rgb(0, 0, 31);
  grid-column: 2/10;
  grid-row: 8/12;
}

.about h2 {
  align-self: flex-end;
}

.contact {
  background-color: $yellow;
  color: rgb(0, 0, 31);
  grid-column: 10/17;
  grid-row: 12/16;
}

.message {
  grid-column: 2/10;
  grid-row: 12/16;
  color: red;
}

@media screen and (min-width: 568px) {
  .grid-container::before {
    grid-row: 1/4;
  }

  .title {
    grid-row: 4/10;
  }

  .projects,
  .about,
  .contact,
  .message {
    grid-row: 10/14;
  }

  .projects {
    grid-column: 9/13;
  }

  .contact {
    grid-column: 13/17;
  }

  .about {
    grid-column: 5/9;
  }

  .message {
    grid-column: 1/5;
    padding: 0 1em;
  }
}

@media screen and (min-width: 768px) {
  .title {
    grid-column: 1/17;
    grid-row: 4/8;
  }

  .about,
  .projects {
    grid-row: 8/12;
  }

  .about {
    grid-column: 5/11;
  }

  .projects {
    grid-column: 11/17;
  }

  .contact {
    grid-column: 11/17;
    grid-row: 12/16;
  }

  .message {
    grid-column: 5/10;
    grid-row: 13;
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
    grid-column: 2/13;
  }

  .title::before {
    content: '';
    display: block;
    position: absolute;
    top: 0;
    right: 12.5vw;
    height: 18.75vh;
    width: 12.5vw;
    background-color: $warm-gray-dark;
  }

  .title {
    grid-column: 2/15;
  }

  .about {
    grid-column: 7/11;
  }

  .about,
  .projects {
    grid-row: 8/14;
  }

  .projects {
    grid-column: 11/15;
  }

  .contact {
    grid-column: 7/15;
    grid-row: 14/17;
  }

  .message {
    grid-column: 3/6;
    grid-row: 10;
  }
}
</style>
