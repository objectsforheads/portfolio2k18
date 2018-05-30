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
    <nav>
      <Btn type="link" router="about" href="#about">
        About
      </Btn>
      <Btn type="link" router="about" href="#ytd">
        Year to Date
      </Btn>
      <Btn type="link" router="about" href="#blog">
        Blog
      </Btn>
    </nav>
  </div>
</template>

<script>
import Btn from '@/components/Button';

export default {
  name: 'Marquee',
  components: { Btn }
}
</script>

<style lang="scss">
@import '@/styles/variables/colors.scss';

[data-component="marquee"] {
  background: color(black);
  min-height: 100vh;
  max-width: 100vw;
  overflow: hidden;
  display: flex;
  align-items: center;
  justify-content: center;
  flex-direction: column;

  > .title {
    filter: drop-shadow(0.125em 0.125em 0 black);
    margin: 0;
    text-transform: uppercase;
    font-size: 2.5rem;
    font-weight: 700;
    text-align: center;
    transform: translate(-1em, 0);
    color: color(white);
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
    transform: translate(2em, -0.4em);
  }

  .small-caps {
    font-size: 0.5em;
    font-weight: 900;
    align-self: flex-start;
    border-bottom: 0.2em solid color(white);
    margin-top: 0.25em;
  }
}
</style>
