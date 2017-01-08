<template>
  <div class="account-widget">

    <div class="account-widget__header">
      <img class="account-widget__header-logo" src="../assets/logo.png">
      <div class="account-widget__header-title">Vue.js account widget</div>
    </div>

    <div class="account-widget__tabs-container">
      <ul class="account-widget__tabs">
        <li class="account-widget__tab" :class="{ 'account-widget__tab_current': isActive('login-form') }">
          <a class="account-widget__tab-link" href="#" @click="selectForm('login-form')">Log In</a>
        </li>
        <li class="account-widget__tab" :class="{ 'account-widget__tab_current': isActive('signup-form') }">
          <a class="account-widget__tab-link" href="#" @click="selectForm('signup-form')">Sign Up</a>
        </li>
      </ul>
    </div>

    <component :is="currentForm"></component>
  </div>
</template>

<script>
  import LoginForm from './LoginForm';
  import SignupForm from './SignupForm';

  export default {
    name: 'account-widget',
    components: {
      LoginForm,
      SignupForm,
    },
    data() {
      return {
        currentForm: 'login-form',
      };
    },
    methods: {
      selectForm(item) {
        // When a model is changed, the view will be automatically updated.
        this.currentForm = item;
      },
      isActive(form) {
        return this.currentForm === form;
      },
    },
  };
</script>

<style scoped>

  .account-widget {
    border-radius: 5px;
    box-shadow: 0 0 40px 4px #111118;
    margin: 80px auto;
    width: 300px;
    background-color: #ffffff;
  }

  .account-widget__header {
    height: 118px;
    background: #f1f1f1;
    padding: 11px;
    color: #333;
    position: relative;
    border-radius: 5px 5px 0 0;
    box-sizing: border-box;
    text-align: center;
  }

  .account-widget__header-logo {
    width: auto;
    height: 60px;
    display: inline-block;
    margin: 0 0 11px;
    vertical-align: middle;
  }

  .account-widget__header-title {
    font-size: 22px;
    box-sizing: initial;
  }

  .account-widget__tabs-container {
    height: 40px;
  }

  .account-widget__tabs {
    background: #fff;
    padding: 0;
    margin: 0;
    font-size: 13px;
    letter-spacing: 0.7px;
    box-shadow: 0 1px 0 0 rgba(92, 102, 111, 0.2);
    display: -webkit-box;
    display: -ms-flexbox;
    display: flex;
    flex-direction: row;
    flex-wrap: wrap;
    justify-content: center;
    align-content: center;
    align-items: stretch;
  }

  .account-widget__tab {
    width: 50%;
    display: block;
    list-style: none;
    float: left;
    padding: 0;
    margin: 0;
    text-align: center;
    cursor: pointer;
  }

  .account-widget__tab-link {
    padding: 11px 10px;
    display: block;
    text-decoration: none !important;
    color: rgba(92, 102, 111, 0.6);
    font-weight: 500;
  }

  .account-widget__tab_current {
    box-shadow: 0 1px 0 0 #5c666f;
    cursor: default;
  }

  .account-widget__tab_current a {
    color: #5c666f;
  }

</style>
