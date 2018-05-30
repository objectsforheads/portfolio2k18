<template>
  <a :href="href" data-component="a" :target="target" :rel="rel">
    <slot />
  </a>
</template>

<script>
export default {
  name: 'Link',
  props: ['href'],
  computed: {
    target: function () {
      try {
        return this.isExternal(this.href) ? '_blank' : null;
      } catch (e) {
        return null;
      }
    },
    rel: function () {
      try {
        return this.isExternal(this.href) ? 'external' : null;
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

[data-component="a"] {
  @include pixel(2);
  color: color(red);
  text-decoration: none;
  line-height: 1;

  &:hover {
    background: color(red);
    text-decoration: none;
    color: color(white);
  }
}
</style>
