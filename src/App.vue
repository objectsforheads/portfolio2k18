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
</style>
