<template>
  <button v-if="type === 'button'" class="btn__wrapper">
    <div class="btn">
      <slot />
    </div>
  </button>
  <a v-else-if="type === 'link'" :href="href" :target="target" :rel="rel" class="btn__wrapper">
    <div class="btn">
      <slot />
    </div>
  </a>
</template>

<script>
export default {
  props: ['type', 'href'],
  computed: {
    target: function () {
      try {
        return this.isExternal(this.link) ? '_blank' : null;
      } catch (e) {
        return null;
      }
    },
    rel: function () {
      try {
        return this.isExternal(this.link) ? 'external' : null;
      } catch (e) {
        return null;
      }
    }
  },
  methods: {
    isExternal: function (link) {
      return link.host !== window.location.host;
    }
  }
}
</script>

<style lang="scss">
@import '~@/styles/fonts.scss';
@import '@/styles/variables/colors.scss';

.btn__wrapper {
  margin: 0.25em;
  display: inline-block;

  &:hover {
    .btn {
      transform: translateY(0.45em);
      border-width: 0.15em 0.2em 0.15em 0.2em;
    }
  }
}

$btn__bg: color(green);
$btn__text: color(white);

.btn {
  padding: 0.25em 0.5em 0.175em 0.5em;
  border-style: solid;
  border-width: 0.15em
                0.2em
                0.6em
                0.2em;
  border-color: darken($color: $btn__bg, $amount: 5)
                darken($color: $btn__bg, $amount: 12)
                darken($color: $btn__bg, $amount: 20)
                darken($color: $btn__bg, $amount: 10);
  display: inline-block;
  // @include pixel(2);
  font-size: 2em;
  text-transform: uppercase;
  font-weight: 900;
  color: $btn__text;
  text-decoration: none;
  background: $btn__bg;
}
</style>
