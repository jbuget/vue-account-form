<template>
  <div class="signup-form">
    <form>

      <!-- Input fields -->
      <section class="signup-form__section signup-form__section_fields">
        <div class="signup-form__field-wrapper">
          <div class="signup-form__field signup-form__field_email">
            <span class="signup-form__field-icon"><i class="material-icons">perm_identity_outline</i></span>
            <input class="signup-form__field-input" type="text" name="first-name" placeholder="your first name">
          </div>
        </div>

        <div class="signup-form__field-wrapper">
          <div class="signup-form__field signup-form__field_email">
            <span class="signup-form__field-icon"><i class="material-icons">perm_identity_outline</i></span>
            <input class="signup-form__field-input" type="text" name="last-name" placeholder="your last name">
          </div>
        </div>

        <div class="signup-form__field-wrapper">
          <div class="signup-form__field signup-form__field_email">
            <span class="signup-form__field-icon"><i class="material-icons">mail_outline</i></span>
            <input class="signup-form__field-input" type="email" name="email" placeholder="your.email@example.com">
          </div>
        </div>

        <div class="signup-form__field-wrapper">
          <div class="signup-form__field signup-form__field_password">
            <span class="signup-form__field-icon"><i class="material-icons">lock_outline</i></span>
            <input class="signup-form__field-input" type="password" name="password" placeholder="your password">
          </div>
        </div>
      </section>

      <!-- Terms of use -->
      <section class="signup-form__section signup-form__section_terms">
        <p>By signing up, you agree to our <a href="#" target="_new">terms of service</a> and <a href="#" target="_new">privacy
          policy</a>.</p>
      </section>

      <!-- Actions -->
      <section class="signup-form__section signup-form__section_actions">
        <button class="signup-form__action signup-form__action_signup">
          <span class="signup-form__action-label">Sign up</span>
          <i class="signup-form__action-icon material-icons">keyboard_arrow_right</i>
        </button>
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

  .signup-form__section_fields {
    padding: 20px;
    box-sizing: border-box;
  }

  .signup-form__field-wrapper {
    margin-bottom: 10px;
  }

  .signup-form__field {
    padding-left: 40px;
    position: relative;
    border-radius: 3px;
    border: 1px solid #f1f1f1;
    background: #f1f1f1;
    -webkit-transition: border-color 0.8s;
    transition: border-color 0.8s;
  }

  .signup-form__field-icon {
    position: absolute;
    font-size: 12px;
    top: 8px;
    left: 9px;
    color: #888;
  }

  .signup-form__field_focused {
    border-color: #a0a0a0;
  }

  .signup-form__field_password {
    margin-bottom: 0;
  }

  .signup-form__field-input {
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

  .signup-form__action_signup {
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

  .signup-form__action-label {
    height: 42px;
    line-height: 42px;
    vertical-align: middle;
  }

  .signup-form__action-icon {
    height: 42px;
    line-height: 42px;
    vertical-align: middle;
  }

</style>
