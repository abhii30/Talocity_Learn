<script></script>

<template>
  <div class="landing">
    <div class="landingLeft">hello</div>
    <div class="landingRight">
      <div class="loginContainer">
        <form action="" class="loginForm">
          <img src="./icons/Logo_Talocity.png" alt="" />
          <h2>Login</h2>
          <h3>Welcome back</h3>
          <div class="inputContainer">
            <label for="Email">Email Address </label>
            <input type="email" id="Email" />
          </div>
          <div class="inputContainer">
            <div class="labelContainer">
              <label for="Password" class="labelLeft">Password </label>
              <label for="Forgot Password" class="labelRight"
                ><a href="#">Forgot password?</a></label
              >
            </div>

            <input type="password" id="password" />
          </div>
          <button type="submit">Login</button>
          <p>Don't have an account?  <a href="#">Contact Sales</a></p>
        </form>
      </div>
    </div>
  </div>
</template>

<style lang="scss">
@import "./Landing.scss";
</style>
