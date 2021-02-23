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
  background-image: linear-gradient(
    rgba(0, 0, 31, 0.5),
    rgba(0, 0, 31, 0.5),
    rgba(0, 0, 31, 0.5),
    rgba(0, 0, 31, 0.5),
    rgba(255, 255, 240, 0.5)
  );
}

.container {
  width: calc(100% - 70px);
  margin: 35px auto 0;
  min-height: 100vh;
}

.page-title {
  color: #56b7eb;
}
</style>
