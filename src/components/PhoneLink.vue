<template>
  <a :href="phoneNumber" class="phone-link">{{ phone }}</a>
</template>

<script>
export default {
  name: 'PhoneLink',
  props: {
    phone: {
      type: String,
      required: true,
    },
  },
  computed: {
    phoneNumber() {
      return this.phone.replace(/[^+\d]/g, '');
    },
  },
};
</script>

<style lang="scss" scoped>
  .phone-link {
    font-weight: bold;
    font-size: 1.38em;
    line-height: 1.22em;
    letter-spacing: 0.03em;
    color: #333333;
  }
</style>
