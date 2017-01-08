<template>
  <div id="app">
    <div class="overlay"></div>
    <account-widget></account-widget>
  </div>
</template>

<script>
import AccountWidget from './components/AccountWidget';

export default {
  name: 'app',
  components: {
    AccountWidget,
  },
};
</script>

<style>

  /*
   * Global styles
   */
  button {
    cursor: pointer;
  }

  button:focus,
  input:focus,
  textarea:focus {
    outline: none;
  }

  /*
   * App styles
   */
  .overlay {
    background: radial-gradient(#40404b, #111118) rgba(34,34,40,0.94);
    opacity: 0.9;
    position: fixed;
    top: 0;
    bottom: 0;
    right: 0;
    left: 0;
    z-index: -1;
  }

</style>
