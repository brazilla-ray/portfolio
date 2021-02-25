<template>
  <div>
    <Nuxt />
  </div>
</template>

<style>
html {
  font-family: 'Alata', 'Source Sans Pro', -apple-system, BlinkMacSystemFont,
    'Segoe UI', Roboto, 'Helvetica Neue', Arial, sans-serif;
  font-size: 16px;
  word-spacing: 1px;
  -ms-text-size-adjust: 100%;
  -webkit-text-size-adjust: 100%;
  -moz-osx-font-smoothing: grayscale;
  -webkit-font-smoothing: antialiased;
  box-sizing: border-box;
}

*,
*::before,
*::after {
  box-sizing: border-box;
  margin: 0;
}

body {
  background-color: #00001f;
}

.container {
  width: calc(100% - 70px);
  margin: 35px auto 35px;
  min-height: 100vh;
}

.page-title {
  color: #56b7eb;
  margin-top: 35px;
}

.section-title {
  color: #56b7eb;
  margin-top: 35px;
  font-size: 1em;
}

.section-content {
  color: #fffff0;
  font-size: 1em;
  display: flex;
  flex-flow: column wrap;
  align-items: center;
}

@media screen and (min-width: 1024px) {
  .container {
    width: 100%;
    margin: auto 0;
  }
}
</style>
