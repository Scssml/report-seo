<template>
  <div class="info-block">
    <div class="info-block__arrow"></div>
    <div class="info-block__content">
      <div class="info-block__name">{{ name }}</div>
      <div class="info-block__value">{{ value }}</div>
      <div class="info-block_text">{{ text }}</div>
    </div>
  </div>
</template>

<script>
export default {
  props: {
    name: {
      type: String,
      required: true,
    },
    value: {
      type: String,
      required: true,
    },
    text: {
      type: String,
      required: true,
    },
    hint: {
      type: String,
      required: true,
    },
    arrow: {
      type: String,
      required: true,
    },
  },
};
</script>
