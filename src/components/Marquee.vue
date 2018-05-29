<template>
  <div data-component="marquee">
    <h1 class="title">
      <div class="top">
        <div data-text="objects">
          Objects
        </div>
      </div>
      <div class="bottom">
        <div data-text="for">
          <span class="uppercase">F</span><span class="small-caps">or</span>
        </div>
        <div data-text="heads">
          Heads
        </div>
      </div>
    </h1>
  </div>
</template>

<script>
export default {
  name: 'Marquee'
}
</script>

<style lang="scss">
@import '@/styles/variables/colors.scss';

[data-component="marquee"] {
  min-height: 100vh;
  width: 100vw;
  overflow: hidden;
  display: flex;
  align-items: center;
  justify-content: center;

  > .title {
    margin: 0;
    text-transform: uppercase;
    font-size: 5rem;
    font-weight: 700;
    text-align: center;
    transform: translate(-1em, 0);
  }

  [data-text] {
    display: flex;
  }

  .top {
    font-size: 1.325em;
    font-weight: 500;
  }

  .bottom {
    display: flex;
    align-items: center;
    justify-content: center;
    transform: translate(2em, -0.2em);
  }

  .small-caps {
    font-size: 0.5em;
    font-weight: 900;
    align-self: flex-start;
    border-bottom: 0.2em solid black;
    margin-top: 0.125em;
  }
}
</style>
