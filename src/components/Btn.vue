<template>
  <a :href="href" class="btn">{{ name }}</a>
</template>

<script>
export default {
  name: 'Btn',
  props: {
    name: {
      type: String,
      required: true,
    },
    href: {
      type: String,
      required: false,
      default: '#',
    },
  },
};
</script>

<style lang="scss" scoped>
  .btn {
    display: inline-flex;
    justify-content: center;
    align-items: center;
    font-weight: 500;
    font-size: 0.79rem;
    line-height: 1.2em;
    text-align: center;
    min-width: 11.73em;
    height: 3.46em;
    background-color: #5B95F5;
    color: #fff;
    text-transform: none;
    border-radius: 3.33em;

    &:hover,
    &:focus {
      text-decoration: none;
      color: #fff;
    }
  }
</style>
