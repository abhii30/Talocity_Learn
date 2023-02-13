<script></script>

<template>
  <div class="landing">
    <div class="landingLeft">
      <div class="col3">
        <div class="box1"><img src="./icons/1.png" alt="" /></div>
        <div class="box1">
          <div class="boxColor" style="background-color: #e7fafe"></div>
        </div>
        <div class="box1"><img src="./icons/2.png" alt="" /></div>
      </div>
      <div class="col3">
        <div class="box1">
          <div class="boxColor" style="background-color: #f3f2ff"></div>
        </div>
        <div class="box1"><img src="./icons/3.png" alt="" /></div>
        <div class="box1">
          <div class="col2">
            <div class="row2">
              <div class="boxColor" style="background-color: #e2e3fe"></div>
            </div>
            <div class="row2"></div>
          </div>
          <div class="col2">
            <div class="row2"></div>
            <div class="row2"><img src="./icons/4.png" alt="" /></div>
          </div>
        </div>
      </div>
      <div class="col3">
        <div class="box1">
          <div class="col2">
            <div class="row2"></div>
            <div class="row2"><img src="./icons/5.png" alt="" /></div>
          </div>
          <div class="col2">
            <div class="row2"></div>
            <div class="row2"></div>
          </div>
        </div>
        <div class="box1">
          <div class="col2">
            <div class="row2"></div>
            <div class="row2">
              <div class="boxColor" style="background-color: #dffcfe"></div>
            </div>
          </div>
          <div class="col2">
            <div class="row2">
              <div class="boxColor" style="background-color: #e2e3fe"></div>
            </div>
            <div class="row2"></div>
          </div>
        </div>
        <div class="box1">
          <div class="col2">
            <div class="row2"><img src="./icons/6.png" alt="" /></div>
            <div class="row2"></div>
          </div>
          <div class="col2">
            <div class="row2"></div>
            <div class="row2"></div>
          </div>
        </div>
      </div>
    </div>
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
          <p>Don't have an account? <a href="#">Contact Sales</a></p>
        </form>
      </div>
    </div>
  </div>
</template>

<style lang="scss">
@import "./Landing.scss";
</style>
