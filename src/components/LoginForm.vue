<template>
  <div class="login-form">
    <form>

      <!-- Input fields -->
      <section class="login-form__section login-form__section_fields">
        <div class="login-form__field login-form__field_email">
          <span></span>
          <input class="login-form__field-input" type="email" name="email" placeholder="your.email@example.com">
        </div>

        <div class="login-form__field login-form__field_password">
          <span></span>
          <input class="login-form__field-input" type="password" name="password" placeholder="your password">
        </div>

        <p class="login-form__forgotten-password">
          <a class="login-form__forgotten-password-link" href="#">Don't remember your password?</a>
        </p>
      </section>

      <!-- Actions -->
      <section class="login-form__section login-form__section_actions">
        <button class="login-form__action login-form__action_login"><span>Log in</span></button>
      </section>

    </form>
  </div>
</template>

<script>
  export default {
    name: 'login-form',
    data() {
      return {
        email: '',
        password: '',
      };
    },
  };
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
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
    color: rgba(0,0,0,0.54);
  }

  .login-form__forgotten-password-link {
    font-size: 13px;
    color: rgba(0,0,0,0.87);
    cursor: pointer;
    margin-bottom: 0;
    text-decoration: none;
  }

  .login-form__field {
    position: relative;
    margin-bottom: 10px;
    border-radius: 3px;
    border: 1px solid #f1f1f1;
    background: #f1f1f1;
    -webkit-transition: border-color 0.8s;
    transition: border-color 0.8s;
  }

  .login-form__field_focused {
    border-color: #a0a0a0;
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


</style>
