<template>
  <div class="login-form">

      <!-- Input fields -->
      <section class="login-form__section login-form__section_fields">
        <div class="login-form__field-wrapper">
          <div class="login-form__field login-form__field_email" :class="{ 'login-form__field--error': hasEmailError }">
            <span class="login-form__field-icon"><i class="material-icons">mail_outline</i></span>
            <input class="login-form__field-input"
                   type="email"
                   name="email"
                   placeholder="your.email@example.com"
                   v-model="email">
          </div>
        </div>

        <div class="login-form__field-wrapper">
          <div class="login-form__field login-form__field_password" :class="{ 'login-form__field--error': hasPasswordError }">
            <span class="login-form__field-icon"><i class="material-icons">lock_outline</i></span>
            <input class="login-form__field-input"
                   type="password"
                   name="password"
                   placeholder="your password"
                   v-model="password">
          </div>
        </div>

        <p class="login-form__forgotten-password">
          <a class="login-form__forgotten-password-link" href="#">Don't remember your password?</a>
        </p>
      </section>

      <!-- Actions -->
      <section class="login-form__section login-form__section_actions">
        <button class="login-form__action login-form__action_login" @click="login">
          <span class="login-form__action-label">Log in</span>
          <i class="login-form__action-icon material-icons">keyboard_arrow_right</i>
        </button>
      </section>

  </div>
</template>

<script>

  function isEmpty(object) {
    if (typeof object === 'object') {
      return Object.keys(object).length === 0;
    }
    if (typeof object === 'string') {
      return object.length === 0;
    }
    throw new Error('Unknown type');
  }

  function isEmailValid(email) {
    // eslint-disable-next-line
    const pattern = /[a-z0-9!#$%&'*+/=?^_`{|}~-]+(?:\.[a-z0-9!#$%&'*+/=?^_`{|}~-]+)*@(?:[a-z0-9](?:[a-z0-9-]*[a-z0-9])?\.)+[a-z0-9](?:[a-z0-9-]*[a-z0-9])?/;
    return pattern.test(email);
  }

  function isPasswordValid(password) {
    return password.length > 5;
  }

  export default {

    name: 'login-form',

    data() {
      return {
        email: '',
        password: '',
        errors: {},
      };
    },

    computed: {
      hasEmailError() {
        return !!this.errors.email;
      },
      hasPasswordError() {
        return !!this.errors.password;
      },
    },

    methods: {
      login() {
        this.errors = {};

        // check email
        if (isEmpty(this.email)) {
          this.errors.email = 'Can\'t be blank';
        } else if (!isEmailValid(this.email)) {
          this.errors.email = 'Must be a valid email';
        }

        // check password
        if (isEmpty(this.password)) {
          this.errors.password = 'Can\'t be blank';
        } else if (!isPasswordValid(this.password)) {
          this.errors.password = 'Must be at least 6 characters';
        }

        if (isEmpty(this.errors)) {
          // TODO login is ok
          console.log('YEAH!');
        }
      },
    },
  };
</script>

<style scoped>

  .login-form__section_fields {
    padding: 20px;
    box-sizing: border-box;
  }

  .login-form__forgotten-password {
    margin-top: 20px;
    margin-bottom: 0;
    font-size: 13px;
    line-height: 1.8;
    text-align: center;
    color: rgba(0, 0, 0, 0.54);
  }

  .login-form__forgotten-password-link {
    font-size: 13px;
    color: rgba(0, 0, 0, 0.87);
    cursor: pointer;
    margin-bottom: 0;
    text-decoration: none;
  }

  .login-form__field-wrapper {
    margin-bottom: 10px;
  }

  .login-form__field {
    padding-left: 40px;
    position: relative;
    border-radius: 3px;
    border: 1px solid #f1f1f1;
    background: #f1f1f1;
    -webkit-transition: border-color 0.8s;
    transition: border-color 0.8s;
  }

  .login-form__field--focused {
    border-color: #a0a0a0;
  }

  .login-form__field--error {
    border-color: red;
  }

  .login-form__field-icon {
    position: absolute;
    font-size: 12px;
    top: 8px;
    left: 9px;
    color: #888;
  }

  .login-form__field_password {
    margin-bottom: 0;
  }

  .login-form__field-input {
    border: 0;
    padding: 0 14px;
    right: 0;
    height: 40px;
    font-size: 13px;
    width: 100%;
    border-radius: 0 2px 2px 0;
    box-sizing: border-box;
    position: relative;
    color: rgba(0, 0, 0, 0.87);
  }

  .login-form__action {
    border: 0;
    padding: 14px;
    display: block;
    box-sizing: border-box;
    width: 100%;
    height: 70px;
    overflow: hidden;
    border-radius: 0 0 5px 5px;
    transition: 0.2s ease-in-out;
    color: #fff;
    letter-spacing: 1px;
    font-size: 14px;
    text-transform: uppercase;
  }

  .login-form__action_login {
    background-color: #EA5323;
    border: 0;
    padding: 14px;
    display: block;
    box-sizing: border-box;
    width: 100%;
    height: 70px;
    overflow: hidden;
    border-radius: 0 0 5px 5px;
    -webkit-transition: 0.2s ease-in-out;
    transition: 0.2s ease-in-out;
    color: #fff;
    letter-spacing: 1px;
    font-size: 14px;
    text-transform: uppercase;
  }

  .login-form__action-label {
    height: 42px;
    line-height: 42px;
    vertical-align: middle;
  }

  .login-form__action-icon {
    height: 42px;
    line-height: 42px;
    vertical-align: middle;
  }

</style>
