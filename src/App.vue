<template>
  <div id="app">
    <div class="overlay"></div>
    <signup-form></signup-form>
  </div>
</template>

<script>
import SignupForm from './components/SignupForm';

export default {
  name: 'app',
  components: {
    SignupForm,
  },
};
</script>

<style>

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
