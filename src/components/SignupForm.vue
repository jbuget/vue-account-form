<template>
  <div class="signup-form">

    <div class="signup-form__header">
      <img class="signup-form__header__logo" src="../assets/logo.png">
      <div class="signup-form__header__title">Vue.js account widget</div>
    </div>

    <div class="signup-form__tabs__container">
      <ul class="signup-form__tabs">
        <li class="signup-form__tabs__tab">
          <a class="signup-form__tabs__tab__link" href="#">Log In</a>
        </li>
        <li class="signup-form__tabs__tab signup-form__tabs__tab_current">
          <a class="signup-form__tabs__tab__link" href="#">Sign Up</a>
        </li>
      </ul>
    </div>

    <form>

      <!-- Input fields -->
      <section class="signup-form__section form-section_fields">
        <div class="signup-form__field signup-form__field_first-name signup-form__field_focused">
          <span></span>
          <input class="signup-form__field__input" type="text" name="first-name" placeholder="your first name">
        </div>

        <div class="signup-form__field signup-form__field_last-name">
          <span></span>
          <input class="signup-form__field__input" type="text" name="last-name" placeholder="your last name">
        </div>

        <div class="signup-form__field signup-form__field_email">
          <span></span>
          <input class="signup-form__field__input" type="email" name="email" placeholder="your.email@example.com">
        </div>

        <div class="signup-form__field signup-form__field_password">
          <span></span>
          <input class="signup-form__field__input" type="password" name="password" placeholder="your password">
        </div>
      </section>

      <!-- Terms of use -->
      <section class="signup-form__section signup-form__section_terms">
        <p>By signing up, you agree to our <a href="#" target="_new">terms of service</a> and <a href="#" target="_new">privacy
          policy</a>.</p>
      </section>

      <!-- Actions -->
      <section class="signup-form__section signup-form__section_actions">
        <button class="signup-form__action signup-form__action-action_signup"><span>Sign up</span></button>
      </section>

    </form>
  </div>
</template>

<script>
  export default {
    name: 'signup-form',
    data() {
      return {
        firstName: '',
        lastName: '',
        email: '',
        password: '',
      };
    },
  };
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>

  input:focus {
    outline: none;
  }

  .signup-form {
    border-radius: 5px;
    box-shadow: 0 0 40px 4px #111118;
    margin: 80px auto;
    width: 300px;
    background-color: #ffffff;
  }

  .signup-form__header {
    height: 118px;
    background: #f1f1f1;
    padding: 11px;
    color: #333;
    position: relative;
    border-radius: 5px 5px 0 0;
    box-sizing: border-box;
    text-align: center;
  }

  .signup-form__header__logo {
    width: auto;
    height: 60px;
    display: inline-block;
    margin: 0 0 11px;
    vertical-align: middle;
  }

  .signup-form__header__title {
    font-size: 22px;
    box-sizing: initial;
  }

  .signup-form__tabs__container {
    height: 40px;
  }

  .signup-form__tabs {
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

  .signup-form__tabs__tab {
    width: 50%;
    display: block;
    list-style: none;
    float: left;
    padding: 0;
    margin: 0;
    text-align: center;
    cursor: pointer;
  }

  .signup-form__tabs__tab__link {
    padding: 11px 10px;
    display: block;
    text-decoration: none!important;
    color: rgba(92, 102, 111, 0.6);
    font-weight: 500;
  }

  .signup-form__tabs__tab_current a {
    color: #5c666f;
  }

  .form-section_fields {
    padding: 20px;
    box-sizing: border-box;
  }

  .signup-form__field {
    position: relative;
    margin-bottom: 10px;
    border-radius: 3px;
    border: 1px solid #f1f1f1;
    background: #f1f1f1;
    -webkit-transition: border-color 0.8s;
    transition: border-color 0.8s;
  }

  .signup-form__field_focused {
    border-color: #a0a0a0;
  }

  .signup-form__field_password {
    margin-bottom: 0;
  }

  .signup-form__field__input {
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

  .signup-form__section_terms {
    background: #eee;
    text-align: center;
    display: block;
    font-size: 12px;
    color: rgba(0, 0, 0, 0.54);
    line-height: 22px;
    padding: 10px;
    position: relative;
  }

  .signup-form__action-action_signup {
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

</style>
