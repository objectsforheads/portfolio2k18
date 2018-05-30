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
      transform: translateY(8px);
      border-width: 4px;
    }
  }
}

.btn {
  padding: 0 0.5em 0.175em 0.5em;
  border: 4px solid color(white);
  border-width: 4px 4px 10px 4px;
  display: inline-block;
  @include pixel(2);
  color: color(white);
  text-decoration: none;
}
</style>
