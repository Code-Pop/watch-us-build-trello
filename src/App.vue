<template>
  <div id="app">
    <router-view/>
  </div>
</template>

<style>
@import 'assets/styles/tailwind.postcss';

body, html {
  height: 100%;
}

#app {
  font-family: 'Avenir', Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  height: 100%;
}

.container {
  @apply mx-auto;
}
</style>
