<template>
  <img :src="src" :alt="alt" class="logo">
</template>

<script>
export default {
  name: 'Logo',
  props: {
    src: {
      type: String,
      required: true,
    },
    alt: {
      type: String,
      required: false,
      default: 'logo',
    },
  },
};
</script>

<style lang="scss" scoped>
  .logo {
    max-width: 6.4rem;
    max-height: 3.15rem;
  }
</style>
