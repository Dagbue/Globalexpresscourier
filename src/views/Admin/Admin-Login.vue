<template>
  <form class="logoIn" @submit.prevent="handleSubmit">
    <div class="wrapper">
<!--      <img alt="company logo" src="@/assets/companylogo.svg" class="logo" />-->
      <div class="headline">
        <h2>
          <span class="header-span">Admin-Login</span>
        </h2>
      </div>
      <div class="form">
        <div class="logoIn">
          <div class="form-group">
            <input type="email" placeholder="Email" required name="email" v-model="email"  />
          </div>
          <div class="form-group">
            <input type="password" placeholder="Password" required name="password"  v-model="password" />
          </div>

<!--          <div class="form-group-2">-->
<!--            <input-->
<!--                type="checkbox"-->
<!--                placeholder="Remember-Me"-->
<!--                id="remember-me"-->
<!--                class="checkbox"-->
<!--            />-->
<!--            <label for="remember-me" class="checkbox-text">Remember me</label>-->
<!--            <a  class="forgot-password" @click.prevent="onPostClick2" >Forgot Password</a>-->
<!--          </div>-->

          <button  class="btn btn-white btn-animated">SIGN IN</button>
          <div v-if="error">{{ error }}</div>

<!--          <div class="separator">-->
<!--            <div class="line"></div>-->
<!--            <h2>OR</h2>-->
<!--            <div class="line"></div>-->
<!--          </div>-->

<!--          <div class="create-acc">-->
<!--            <p class="create-text">-->
<!--              Don’t have an account?<a @click.prevent="onPostClick"-->
<!--                                       class="create-link"-->
<!--            >Sign up here</a-->
<!--            >-->
<!--            </p>-->
<!--          </div>-->
        </div>
      </div>
    </div>
  </form>
</template>

<script>
  import { ref } from 'vue'
  import { useStore } from 'vuex'
  import { useRouter } from 'vue-router'
export default {
  name: "Admin-Login",
  // methods: {
  //   onPostClick() {
  //     this.$router.push("/register");
  //     window.scrollTo(0, 0);
  //   },
  //   onPostClick2() {
  //     this.$router.push("/forgot-password");
  //     window.scrollTo(0, 0);
  //   },
  // },
  setup() {
    const email = ref('')
    const password = ref('')
    const error = ref(null)
    const store = useStore()
    const router = useRouter()
    const handleSubmit = async () => {
      try {
        await store.dispatch('login', {
          email: email.value,
          password: password.value
        })
        await router.push('/dash-home')
      }
      catch (err) {
        error.value = err.message
      }
    }
    return { handleSubmit, email, password, error }
  }
}
</script>

<style scoped>

.logo {
  width: 35%;
  margin-left: 30%;
  margin-bottom: 3%;
}


form {
  margin: 5rem auto;
  max-width: 40rem;
  border-radius: 5px;
  /*box-shadow:  30px 30px 100px #bebebe,*/
  /*-50px -50px 100px #ffffff;*/
  /*padding: 2rem;*/
  /*background-color: #ffffff;*/
}

:root {
  --primary-color: #3525d3;
  --white-color: #fff;
  --black-color: #3c4a57;
  --light-gray: #e4e8ee;
}

.wrapper {
  position: relative;
  align-items: center;
  justify-content: center;
}

.header-span {
  color: #ec2552;
}

.wrapper {
  padding: 0 25px 0;
  max-width: 768px;
  width: 100%;
  margin: auto;
}

.wrapper::before {
  content: "";
  position: absolute;
  top: 0;
  left: 0;
  right: 0;
  bottom: 0;
  background-position: center center;
  background-size: cover;
  background-repeat: no-repeat;
  min-height: 100vh;
  z-index: -1;
}

.wrapper .headline {
  text-align: center;
  padding-bottom: 30px;
}

.wrapper .headline h1 {
  font-size: 30px;
  font-weight: 500;
  line-height: 52px;
}

.wrapper .headline h2 {
  font-weight: 400;
  font-size: 28px;
}

.wrapper .form {
  max-width: 350px;
  width: 100%;
  margin: auto;
}

.wrapper .form-group {
  margin-bottom: 15px;
}

.wrapper .form-group input {
  display: block;
  font-size: 16px;
  line-height: 24px;
  letter-spacing: -0.1px;
  padding: 12px 16px;
  height: 48px;
  border-radius: 5px;
  color: var(--black-color);
  border: 1px solid #e4e8ee;
  box-shadow: none;
  width: 100%;
}

.wrapper .form-group input:focus {
  outline: none;
}

.wrapper .form-group input::placeholder {
  color: var(--black-color);
  font-weight: 400;
  font-size: 14px;
}

.btn,
.btn-white,
.btn-animated {
  width: 100%;
  margin: 15px 0 30px;
  line-height: 22px;
  padding: 12px 29px;
  text-transform: uppercase;
  border: none;
  text-align: center;
  border-radius: 5px;
}

.btn:link,
.btn:visited {
  text-transform: uppercase;
  text-decoration: none;
  padding: 10px 20px;
  display: inline-block;
  border-radius: 100px;
  transition: all 0.2s;
  position: relative;
}
.btn:hover {
  background-color: white;
  border: 1px solid #ec2552;
  color: #ec2552;
}
.btn-white {
  background-color: #ec2552;
  border: 1px solid #ec2552;
  color: white;
  font-size: 15px;
}

.separator .line {
  height: 1px;
  flex: 0.5;
  background-color: #676767;
}

.separator h2 {
  padding: 0 1rem;
  font-size: 13px;
  color: #676767;
}


@media (max-width: 1030px) {
  .wrapper::before {
    left: -25%;
    min-height: 60vh;
    height: 500px;
  }
}
@media (max-width: 767px) {
  .wrapper {
    max-width: 550px;
  }
  .wrapper .headline h1 {
    font-size: 22px;
    line-height: 25px;
  }
}
@media (max-width: 990px) {
  .wrapper .headline h1  {
    font-size: 32px;
  }
  .wrapper .headline h2  {
    font-size: 28px;
  }
}
@media (max-width: 500px) {
  .wrapper {
    padding: 10px 25px 0;
  }
  form {
    margin: 1rem;
    max-width: 40rem;
    border-radius: 12px;
    box-shadow: 0 2px 8px rgba(0, 0, 0, 0.26);
    padding: 1rem;
    background-color: #ffffff;
  }
  .wrapper .headline h1  {
    font-size: 25px;
  }
  .wrapper .headline h2  {
    font-size: 23px;
  }
}

</style>