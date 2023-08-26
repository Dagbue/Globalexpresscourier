<template>
  <template v-if="!$route.meta.hideNavigation">
    <div class="topmost-header" v-if="$route.name !== 'DashHome'" >
      <div class="topmost-header-1">
        <p class="topmost-header-text">
          <i class='bx bxs-map' ></i>
          3560 Air Center Cove Ste 101 Memphis, Tennessee, USA
        </p>
        <p class="topmost-header-text">
          <i class='bx bxs-time-five' ></i>Mon – Sat: 9:00am–18:00pm.
        </p>
        <p class="topmost-header-text">
          <i class='bx bxs-phone' ></i>+1760-314-5437
        </p>
      </div>
    </div>
    <div class="style-4" v-if="$route.name !== 'DashHome'" >

      <img alt="company logo" src="../src/assets/companylogo.png" class="logo" />

      <ul class="menu-4" v-show="!mobile">
        <li><router-link  to="/">HOME</router-link></li>
        <li><router-link  to="/about">ABOUT US</router-link></li>
        <li><router-link  to="/services">SERVICES</router-link></li>
        <li><router-link  to="/contact">CONTACT</router-link></li>
        <li><router-link to="/pricing">PRICING</router-link></li>
        <li><router-link  to="/tracking">TRACKING</router-link></li>
        <li><router-link  to="/quote">REQUEST A QUOTE</router-link></li>
      </ul>

      <transition name="mobile-nav">

        <ul class="dropdown-nav" v-show="mobileNav">
          <li @click="toggleMobileNav2"><router-link  to="/">HOME</router-link></li>
          <li @click="toggleMobileNav2"><router-link  to="/about">ABOUT</router-link></li>
          <li @click="toggleMobileNav2"><router-link  to="/services">SERVICES</router-link></li>
          <li @click="toggleMobileNav2"><router-link  to="/contact">CONTACT</router-link></li>
          <li @click="toggleMobileNav2"><router-link to="/pricing">PRICING</router-link></li>
          <li @click="toggleMobileNav2"><router-link  to="/tracking">TRACKING</router-link></li>
          <li @click="toggleMobileNav2"><router-link  to="/quote">REQUEST A QUOTE</router-link></li>
        </ul>


      </transition>

      <div class="icon">
        <i @click="toggleMobileNav" class='bx bx-menu' v-show="mobile" :class="{'icon-active' : mobileNav}"></i>
      </div>

    </div>
  </template>

  <router-view v-slot="{ Component }">
    <transition name="route" mode="out-in">
      <component :is="Component"></component>
    </transition>
  </router-view>

</template>

<script>


export default {
  data()  {
    return {
      value1: false,
      mobile: false,
      mobileNav: false,
      windowWidth: false,
    }
  },
  created() {
    window.addEventListener('resize', this.checkScreen);
    this.checkScreen();
  },
  methods: {
    toggleMobileNav() {
      this.mobileNav = !this.mobileNav;
    },
    toggleMobileNav2(){
      this.mobileNav = false;
    },
    checkScreen() {
      this.windowWidth = window.innerWidth;
      if (this.windowWidth <= 990){
        this.mobile = true;
        return;
      }
      this.mobile = false;
      this.mobileNav = false;
      return;
    },

  }

};
</script>


<style>

* {
  margin: 0;
  padding: 0;
  box-sizing: border-box;
}
body{
  cursor: pointer;
  counter-reset: Serial;
  font-family: 'Outfit', sans-serif;
}
/* Chrome, Safari, Edge, Opera */
input::-webkit-outer-spin-button,
input::-webkit-inner-spin-button {
  -webkit-appearance: none;
  margin: 0;
}
/* Firefox */
input[type=number] {
  -moz-appearance: textfield;
}
a{
  text-decoration: none;
  cursor: pointer;
}

.logo {
  height: 8%;
  width: 11%;
  margin-left: 4%;
}
.style-4 {
  display: flex;
  align-items: center;
  align-content: center;
  padding-left: 5%;
}

.menu-4 {
  padding-left: 2.5%;
}

.menu-4 * {
  box-sizing: border-box;
  -webkit-transition: all 0.35s ease;
  transition: all 0.35s ease;
}
.menu-4 li {
  display: inline-block;
  list-style: outside none none;
  margin: 0 1.6em;
  overflow: hidden;
  padding-right: 8px;
  padding-left: 20px;
  font-weight: bold;
  font-size: 12px;
}
.menu-4 a {
  padding: 0.3em 0;
  color: #676767;
  position: relative;
  display: inline-block;
  letter-spacing: 1px;
  margin: 0;
  text-decoration: none;
}

.menu-4 a:before,
.menu-4 a:after {
  position: absolute;
  -webkit-transition: all 0.35s ease;
  transition: all 0.35s ease;
}

.menu-4 a:before {
  bottom: 100%;
  display: block;
  height: 3px;
  width: 100%;
  content: "";
}

.menu-4 a:after {
  padding: 0.3em 0;
  position: absolute;
  bottom: 100%;
  left: 0;
  content: attr(data-hover);
  color: #676767;
  white-space: nowrap;
}

.menu-4 li:hover a,
.menu-4 .current a {
  color: #ec2552;
}

.route-enter-from {
  opacity: 0;
  transform: translateX(100px);
}
.route-enter-active {
  transition: all 1s ease-out;
}
.route-leave-to {
  opacity: 0;
  transform: translateX(-100px);
}
.route-leave-active {
  transition: all 1s ease-in;
}

.topmost-header {
  background-color: #192744;
  padding-top: 10px;
  padding-bottom: 10px;
  color: white;
  display: flex;
  box-shadow: 0 0 20px rgba(0, 0, 0, 0.1);
}

.topmost-header-1 {
  display: flex;
  margin-left: 12%;
}

.topmost-header-text {
  font-size: 13px;
  padding-right: 28px;
  display: flex;
  align-content: center;
  align-items: center;
}
i{
  padding-right: 4px;
  font-size: 15px;
  color: #ec2552;
}

.dropdown-nav{
  display: flex;
  list-style: none;
  flex-direction: column;
  position: fixed;
  top: 0;
  left: 0;
  z-index: 99;
  padding-right: 7%;
  width: 100%;
  max-width: 300px;
  height: 100%;
  background-color: #192744;
  font-size: 20px;
  text-align: center;
}

.dropdown-nav li {
  margin-top: 8%;
  overflow: hidden;
  list-style: none;
  font-weight: bold;
  height: 100%;
}

.dropdown-nav * {
  box-sizing: border-box;
  -webkit-transition: all 0.35s ease;
  transition: all 0.35s ease;
}
.dropdown-nav a {
  padding: 0.3em 0;
  color: #676767;
  position: relative;
  display: inline-block;
  letter-spacing: 1px;
  margin: 0;
  text-decoration: none;
}

.dropdown-nav a:before,
.dropdown-nav a:after {
  position: absolute;
  -webkit-transition: all 0.35s ease;
  transition: all 0.35s ease;
}

.dropdown-nav a:before {
  bottom: 100%;
  display: block;
  height: 3px;
  width: 100%;
  content: "";
  background-color: #ec2552;
}

.dropdown-nav a:after {
  padding: 0.3em 0;
  position: absolute;
  bottom: 100%;
  left: 0;
  content: attr(data-hover);
  color: #676767;
  white-space: nowrap;
}

.dropdown-nav li:hover a,
.dropdown-nav.current a {
  color: #ec2552;
}

hr {
  color: white;
  width: 100%;
  background-color: white;
  border: 1px solid white;
  margin-top: 95px;
}


.mobile-nav-enter-active,
.mobile-nav-leave-active {
  transition: 1s ease all;
}

.mobile-nav-enter-from,
.mobile-nav-leave-to{
  transform: translateX(-250px);
}

.mobile-nav-enter-to{
  transform: translateX(0);
}



@media (min-width: 1286px) {
  .hamburger {
    display: none;
  }
}

@media (max-width: 990px) {
  .style-4 {
    display: flex;
    align-content: center;
    align-items: center;
    justify-content: space-between;
  }
  .bx-menu{
    font-size: 43px;
  }
  .logo {
    width: 18%;
    margin-left: unset;
  }
}

@media (max-width: 861px) {
  .topmost-header {
    display: none;
  }
}

@media (max-width: 550px) {
  .bx-menu{
    font-size: 43px;
  }
  .logo {
    margin-top: 1%;
    width: 35%;
    margin-left: unset;
  }

  .dropdown-nav{
    padding-right: 10%;
    max-width: 230px;
    font-size: 12px;
  }

  .dropdown-nav li {
    margin-top: 8%;
  }

  hr {
    margin-top: 95%;
  }

}

</style>