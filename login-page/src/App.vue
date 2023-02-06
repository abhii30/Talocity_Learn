<script>
export default {
  methods: {
    recruiter() {
      document.getElementById("rec").style.left = "0";
      document.getElementById("btn").style.left = "50%";
      document.getElementById("can").style.left = "-101%";
    },
    candidate() {
      document.getElementById("can").style.left = "0%";
      document.getElementById("btn").style.left = "0%";
      document.getElementById("rec").style.left = "101%";
    },
  },
};
</script>

<template>
  <main>
    <div class="form-box">
      <h2>Login</h2>
      <div class="button-box">
        <div id="btn"></div>
        <button type="button" class="toggle-btn" @click="candidate">
          Candidate
        </button>
        <button type="button" class="toggle-btn" @click="recruiter">
          Recruiter
        </button>
      </div>
      <div class="candidate" id="can">
        <form class="input-group" action="" method="">
          <vue-tel-input v-bind=""></vue-tel-input>
          <label for="cmob">Mobile Number</label>
          <div class="mobile">
            <input type="zipcode" placeholder=" +91" id="zip" />
            <input type="text" placeholder="1234567890" id="cmob" />
          </div>
          <button type="submit" class="submit-btn">Next</button>
          <span
            >Need to login with password? <a href="">Enter Password</a></span
          >
        </form>
      </div>
      <div class="recruiter" id="rec">
        <form class="input-group" action="" id="recruiter">
          <vue-tel-input v-bind=""></vue-tel-input>
          <div class="input-list">
            <label for="email">Email</label>
            <input type="email" placeholder="Enter Registered email" />
          </div>
          <div class="input-list">
            <label for="password">Password</label>
            <input type="password" placeholder="Password" />
          </div>
          <button type="submit" class="submit-btn">Login</button>
          <span> <a href="">Forgot Password?</a></span>
        </form>
      </div>
    </div>
  </main>
</template>

<style scoped>
main {
  height: 100vh;
  display: flex;
  justify-content: center;
  align-items: center;
  color: black;
}

.form-box {
  position: relative;
  width: 40vh;
  height: 60vh;
  background-color: azure;
  padding: 5vh 3vh;
  overflow: hidden;
  text-align: center;
}
h2 {
  text-align: center;
  padding-bottom: 5%;
}
.button-box {
  position: relative;
  height: 5vh;
  position: relative;
  box-shadow: 0 0 10px 5px rgb(199, 199, 199);
  border-radius: 5vh;
  /* display: flex; */
}
.toggle-btn {
  width: 50%;
  cursor: pointer;
  position: relative;
  height: 5vh;
  border: none;
  background: transparent;
  outline: none;
}
.candidate {
  position: absolute;
  width: 100%;
  left: 0;
  padding: 0 3vh;
  transition: 0.5s;
}

.recruiter {
  position: absolute;
  width: 100%;
  left: 101%;
  padding: 0 3vh;
  transition: 0.5s;
}
label {
  text-align: left;
  font-size: 12px;
}
#btn {
  position: absolute;
  z-index: 0;
  top: 0;
  left: 0;
  height: 100%;
  width: 50%;
  background: linear-gradient(to right, rgb(118, 67, 67), rgb(49, 145, 103));
  border-radius: 5vh;
  transition: 0.5s;
}
.input-group {
  margin-top: 15%;
  display: flex;
  flex-direction: column;
  transition: 0.5s;
}
input {
  font-size: 15px;
}
.mobile {
  display: flex;
  flex-direction: row;
}
#zip {
  height: 5vh;
  width: 30%;
  padding: 0 2vh;
  background-color: #cdcdcd;
  border: none;
}
input {
  height: 5vh;
  padding: 0 2vh;
  background-color: #e5e5e5;
  border: none;
}
#cmob {
  width: 70%;
}
.submit-btn {
  position: relative;
  border: none;
  height: 5vh;
  background-color: burlywood;
  border-radius: 5vh;
  margin-top: 10%;
}
span {
  margin-top: 3%;
  font-size: 12px;
}
a {
  text-decoration: none;
}
.input-list {
  display: flex;
  flex-direction: column;
  margin-bottom: 2vh;
}

input:focus {
  outline: none;
  border: 2px solid purple;
}
</style>
