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
}

#app {
  font-family: 'renner', Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  // color: #2c3e50;
  color: color(black);
}

.slide {
  min-height: 100vh;
  max-width: 100vw;
  overflow: hidden;
  display: flex;
  align-items: center;
  justify-content: center;
}

.markdown {
  a {
    @include pixel(2);
    color: red;

    &:hover {
      background: red;
      text-decoration: none;
      color: white;
    }
  }
}
</style>
