<template>
  <div class="select">
    <select>
      <template v-for="(item, index) in options" :key="index">
        <option
          :value="item.value"
        >{{ item.name }}</option>
      </template>
    </select>
  </div>
</template>

<script>
export default {
  name: 'Select',
  props: {
    options: {
      type: Array,
      required: true,
      default: () => [],
    },
  },
};
</script>

<style lang="scss" scoped>
  .select {
    display: flex;
    position: relative;
    justify-content: center;
    align-items: center;
    font-weight: 500;
    font-size: 0.79rem;
    line-height: 1.2em;
    text-align: center;
    min-width: 11.73em;
    height: 3.46em;
    background-color: #5B95F5;
    text-transform: none;
    border-radius: 3.33em;
    padding: 0 1.5em;

    select {
      outline: none;
      appearance: none;
      border: 0;
      width: 100%;
      color: #fff;
      background: transparent;

      option {
        color: #000;
      }
    }

    &:before,
    &:after {
      content: '';
      position: absolute;
      width: 10px;
      height: 1px;
      background: #fff;
      right: 1.5em;
    }

    &:before {
      transform: rotate(45deg) translate(-3px, 2px);
    }

    &:after {
      transform: rotate(-45deg) translate(3px, 2px);
    }

    &--transparent {
      border: 1px solid #5B95F5;
      background: transparent;

      select {
        color: #5B95F5;
      }

      &:before,
      &:after {
        content: '';
        background: #5B95F5;
      }
    }
  }
</style>
