<template>
  <main>
    <Marquee />
    <About />
    <YTD />
  </main>
</template>

<script>
import Marquee from '@/components/Marquee';
import About from '@/components/About';
import YTD from '@/components/YTD';

export default {
  name: 'Homepage',
  components: { Marquee, About, YTD }
}
</script>

<style lang="scss">
@import '~@/styles/fonts.scss';
@import '@/styles/variables/colors.scss';

.slide {
  min-height: 100vh;
  max-width: 100vw;
  overflow: hidden;
  display: flex;
  align-items: center;
  justify-content: center;
  background: color(white);

  .content {
    width: 100%;
    max-width: 32rem;
    padding: 1rem;
  }

    h1 {
    margin: 0;
    @include pixel(5);
    position: fixed;
    bottom: 0;
    left: 0;
    padding: 0.3rem 1rem;
  }

  ul {
    margin: 0;
  }

  .content {
    width: 75%;
    margin-left: auto;
  }
}
</style>
