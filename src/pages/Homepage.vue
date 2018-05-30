<template>
  <main>
    <Marquee />
    <Goodbye />
  </main>
</template>

<script>
import Marquee from '@/components/Marquee';
import Goodbye from '@/components/Goodbye';

export default {
  name: 'Homepage',
  components: { Marquee, Goodbye }
}
</script>

<style lang="scss">
</style>
