<template>
  <router-view/>
</template>

<style lang="scss">
  @import url('https://fonts.googleapis.com/css2?family=Inter:wght@400;500;700&display=swap');

  @import "../node_modules/bootstrap/scss/functions";
  @import "../node_modules/bootstrap/scss/variables";
  @import "../node_modules/bootstrap/scss/mixins";
  @import "../node_modules/bootstrap/scss/reboot";
  @import "../node_modules/bootstrap/scss/grid";
  @import "../node_modules/bootstrap/scss/utilities";

  html, body {
    font-size: 19px;
  }

  body {
    font-family: 'Inter', sans-serif;
    color: #838A92;
    line-height: 1.47rem;
    background-color: #fff;
  }

  a, a:hover, a:focus {
    color: #5B95F5;
  }

  .h1, h1 {
    font-weight: bold;
    font-size: 3rem;
    line-height: 3.63rem;
    color: #333333;
  }

  .color-blue {
    color: #5B95F5;
  }

  .font-weight-500 {
    font-weight: 500 !important;
  }
</style>
