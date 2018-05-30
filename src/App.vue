<template>
  <div id="app">
    <router-view/>
  </div>
</template>

<script>
export default {
  name: 'App'
}
</script>

<style lang="scss">
@import '~@/styles/fonts.scss';
@import '@/styles/variables/colors.scss';

*, *::before, *::after {
  position: relative;
  box-sizing: border-box;
}

body, html {
  margin: 0;
  padding: 0;
  font-size: 32px;
  background: color(white);
  line-height: 1.33;
}

#app {
  font-family: 'renner', Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  color: color(black);
}
</style>
