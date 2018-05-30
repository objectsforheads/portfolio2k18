<template>
  <div data-component="about" class="slide">
    <div class="content">
      <h1 id="about">About</h1>
      <ul>
        <li>Definitely not a mischief of magpies in a trenchcoat</li>
        <li>Sometimes remembers to put work up on <Lnk href="https://www.github.com/objectsforheads">github</Lnk></li>
        <li>Available via carrier pigeon if it hasn't gotten lost again</li>
      </ul>
    </div>
  </div>
</template>

<script>
import Lnk from '@/components/Link';

export default {
  name: 'About',
  components: { Lnk }
}
</script>
