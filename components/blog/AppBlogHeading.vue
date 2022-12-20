<template>
  <section class="intro-sec p-0">
    <div
      id="slider-2-slide-3-layer-1"
      class="tp-shape tp-shapewrapper rs-layer"
      data-type="shape"
      data-rsp_ch="on"
      data-xy="x:c;y:m;"
      data-text="fw:100;a:inherit;"
      data-dim="w:100%;h:100%;"
      data-basealign="slide"
      data-frame_1="o:0.8;sR:10;"
      data-frame_999="o:0;st:w;sR:8690;"
      data-idcheck="true"
      data-stylerecorder="true"
      data-initialised="true"
    ></div>
    <div class="after_intro">
      <img
        style=""
        class="img-fluid"
        src="//the7.io/agency/wp-content/uploads/sites/43/2017/10/art-poly-slider.png"
        alt=""
      />
    </div>
    <div v-tilt="{ tiltMaxAngleY: 10, tiltMaxAngleX: 10 }" class="intro">
      <div class="intro">
        <div class="row m-0 align-items-center justify-content-center">
          <div class="col-auto text-center">
            <img
              src="/assets/images/logo.png"
              alt="logoImage"
              style="width: 250px"
              class="animatedTop"
            />
            <h1 class="animatedLeft">BLOG <span>DETAILS</span></h1>
            <img
              class="scrolldown"
              src="//the7.io/agency/wp-content/uploads/sites/43/2021/09/arrow-down-40.png"
              alt=""
            />
          </div>
        </div>
      </div>
    </div>
    <header :class="!topOfPage ? 'onScroll' : ''">
      <b-navbar toggleable="lg">
        <b-navbar-brand :href="localePath('/')">
          <img
            src="/assets/images/logo.png"
            alt="logoImage"
            style="width: 250px"
            class="navLogo"
          />
        </b-navbar-brand>

        <b-collapse
          id="navbar-toggle-collapse"
          class="ml-auto justify-content-center"
          is-nav
        >
          <b-navbar-nav class="align-items-center">
            <b-nav-item active-class="active" :to="localePath('/')" exact
              >Home</b-nav-item
            >
            <b-nav-item :to="localePath('/services')">Services</b-nav-item>
            <b-nav-item :to="localePath('/faq')">Why Us</b-nav-item>
            <b-nav-item :to="localePath('/contact')">Case Studies</b-nav-item>
            <b-nav-item :to="localePath('/about')">About</b-nav-item>
            <b-nav-item :to="localePath('/blogs')">Blogs</b-nav-item>
            <b-nav-item :to="localePath('/careers')">Career</b-nav-item>
            <b-nav-item :to="localePath('/events')">Events</b-nav-item>
          </b-navbar-nav>
        </b-collapse>
        <div href="#" class="social-header">
          <a href="#">
            <i class="fa-brands fa-facebook-f"></i>
          </a>
          <a href="#">
            <i class="fa-brands fa-twitter"></i>
          </a>
          <a href="#">
            <i class="fa-solid fa-globe"></i>
          </a>
        </div>
        <div>
          <lang-switch></lang-switch>
        </div>
        <div v-if="$store.state.user" class="logout" @click="logout">
          <i class="fa-regular fa-right-from-bracket"></i>
        </div>
        <b-navbar-toggle target="navbar-toggle-collapse">
          <template #default="{ expanded }">
            <span
              class="menu-trigger"
              :class="expanded ? 'active' : ''"
              id="menu03"
            >
              <span></span>
              <span></span>
              <span></span>
            </span>
          </template>
        </b-navbar-toggle>
      </b-navbar>
    </header>
  </section>
</template>

<script>
import langSwitch from "../langSwitch/langSwitch.vue";
import "animate.css/animate.min.css";
export default {
  name: "AppBlogHeading",
  data() {
    return {
      show: false,
      show1: false,
      topOfPage: true,
    };
  },
  components: {
    langSwitch,
  },
  beforeMount() {
    window.addEventListener("scroll", this.handleScroll);
  },
  mounted() {},
  methods: {
    logout() {
      this.$store.commit("setUserData", null);
      this.$cookies.remove("cms-auth");
      this.$cookies.remove("cms-user");
      this.$router.push(this.localePath("/login"));
    },
    handleScroll() {
      let box = document.querySelector(".intro-sec");
      let height = box.offsetHeight;
      if (window.pageYOffset > height) {
        if (this.topOfPage) this.topOfPage = false;
      } else {
        if (!this.topOfPage) this.topOfPage = true;
      }
    },
  },
};
</script>

<style>
@keyframes sdb07 {
  0% {
    transform: translateY(0);
  }
  50% {
    transform: translateY(10px);
  }
  100% {
    transform: translateY(0);
  }
}
.logout {
  width: 50px;
  height: 50px;
  border-radius: 50%;
  background-color: var(--main-color);
  color: #fff;
  display: grid;
  place-items: center;
  font-size: 1.2rem;
  cursor: pointer;
}
.scrolldown {
  -webkit-animation-delay: 0s;
  animation-delay: 0s;
  animation: sdb07 2s infinite;
}
.intro-sec {
  background-color: rgba(255, 255, 255, 0);
  background-image: linear-gradient(
      rgba(0, 0, 0, 0.24) 100%,
      rgb(255, 255, 255) 100%
    ),
    url("https://the7.io/agency/wp-content/uploads/sites/43/2017/10/slider-img-01.jpg");
  background-position: center center;
  background-repeat: no-repeat;
  background-size: cover;
  position: relative;
  min-height: 100vh;
}
.intro {
  padding: 80px 32px 0;
  z-index: 10;
  position: relative;
  height: calc(100vh - 70px);
  min-height: 600px;
}
.intro h1 {
  margin-top: 30px;
  font-size: 100px;
  font-weight: 900;
  letter-spacing: normal;
  line-height: 110px;
  color: #fff;
}
.intro h1 span {
  color: rgb(243, 97, 90);
}
.intro p {
  color: rgb(243, 97, 90);
  display: block;
  margin-top: 30px;
  font-size: 30px;
  font-style: italic;
  font-weight: 900;
}
.intro .btn i {
  margin-left: 12px;
}
.intro .btn:hover {
  color: #fff;
  background-color: transparent;
  border-color: #fff;
}
.intro .form {
  width: 438px;
  max-width: 100%;
  padding: 24px;
  border-radius: 12px;
  box-shadow: rgba(0, 0, 0, 0.1) 0px 24px 32px -6px;
  background: #fff;
  margin-bottom: -50px;
}
.intro .form img {
  height: 80px;
  width: 80px;
  border-radius: 50%;
}
.intro .form h2 {
  font-size: 26px;
  font-weight: 500;
  letter-spacing: -0.416px;
  line-height: 36.4px;
  margin: 12px 0 4px;
}
.intro .form h3 {
  font-size: 19px;
  font-weight: 400;
  line-height: 26.4px;
  margin: 12px 0 4px;
  color: rgb(119, 119, 119);
}
.intro .form .phone {
  text-decoration: none;
  color: rgb(248, 96, 17);
  font-size: 18px;
  font-weight: 500;
  letter-spacing: -0.18px;
  line-height: 21px;
  margin: 0 0 10px;
  padding: 17px 40px;
  display: inline-block;
}
.intro .form svg {
  margin-right: 12px;
}
.intro .form input {
  margin: 8px 0;
  padding: 0 18px;
  color: rgb(94, 94, 94);
  font-size: 18px;
  font-weight: 400;
  height: 60px;
  border-radius: 10px;
  border: 1px solid rgb(219, 219, 219);
  color: rgb(94, 94, 94);
}
.intro .form input::placeholder {
  color: #a7a7a7;
}
.intro .form input:focus {
  border: 1px solid rgb(248, 96, 17);
  box-shadow: none;
}
.intro .form .btn {
  padding: 17px 40px;
  background-color: rgb(248, 96, 17);
  display: block;
  margin: 8px 0;
  font-size: 18px;
  font-weight: 500;
  letter-spacing: -0.18px;
  line-height: 21px;
  text-transform: capitalize;
  border-radius: 10px;
  border: 1px solid rgb(248, 96, 17);
  color: #fff;
}
.intro .form .btn:hover {
  background-color: rgb(153, 63, 15);
  border: 1px solid rgb(153, 63, 15);
}
.intro .form small {
  color: rgb(119, 119, 119);
  font-size: 13px;
  font-weight: 400;
  line-height: 24px;
}
header {
  height: 70px;
  padding: 0 20px;
  transition: all 0.1s ease 0s;
  background-color: rgba(0, 0, 0, 0.3);
  z-index: 10;
  position: relative;
}
header .navbar {
  padding: 0;
}
.navbar-brand {
  padding: 0 50px 0 0;
}
.navbar-brand img {
  max-width: 230px;
}
.nav-item {
  position: relative;
  margin: 0 12px;
}
.nav-item::after {
  content: " ";
  position: absolute;
  left: 18px;
  right: 18px;
  bottom: -24px;
  height: 2px;
  transition: all calc(300 * 1ms) cubic-bezier(0.42, 0.01, 0.58, 1);
  z-index: 999999998;
  background-color: transparent;
}
.nav-item.active::after,
.nav-item:hover:after {
  background-color: rgb(243, 97, 90);
  left: 18px;
  right: 18px;
  bottom: 18px;
}
.nav-link {
  margin: 18px 14px;
  padding: 4px !important;
  font-size: 18px !important;
  font-stretch: 100%;
  font-weight: 700 !important;
  line-height: 22px;
  color: #fff !important;
}
.social-header a {
  color: rgb(243, 97, 90);
  display: inline-flex;
  font-size: 16px;
  height: 28px;
  justify-content: center;
  line-height: 28px;
  margin-right: 2px;
  position: relative;
  text-align: center;
  text-decoration-color: rgb(243, 97, 90);
  text-decoration-line: none;
  width: 28px;
  border: 2px solid rgb(243, 97, 90);
  border-radius: 100px;
  align-items: center;
  transition: all 0.15s linear;
}
.social-header a:hover {
  background-color: rgb(243, 97, 90);
  color: #fff;
}
.navbar-toggler,
.navbar-toggler:focus {
  border: none;
  box-shadow: none;
}
.menu-trigger,
.menu-trigger span {
  display: inline-block;
  transition: all 0.4s;
  box-sizing: border-box;
}
.menu-trigger {
  position: relative;
  width: 20px;
  height: 16px;
  background: none;
  border: none;
  appearance: none;
  cursor: pointer;
}
.menu-trigger span {
  position: absolute;
  left: 0;
  width: 100%;
  height: 3px;
  background-color: #000;
  border-radius: 4px;
}
.menu-trigger span:nth-of-type(1) {
  top: 0;
}
.menu-trigger span:nth-of-type(2) {
  top: 6px;
}
.menu-trigger span:nth-of-type(3) {
  bottom: 0;
}
#menu03.active {
  transform: rotate(360deg);
}
#menu03.active span:nth-of-type(1) {
  transform: translateY(6px) rotate(-45deg);
}
#menu03.active span:nth-of-type(2) {
  transform: translateY(0) rotate(45deg);
}
#menu03.active span:nth-of-type(3) {
  opacity: 0;
}
.onScroll {
  position: fixed !important;
  width: 100%;
  display: flex;
  align-items: center;
  transition: all 0.2s ease-in-out;
  box-shadow: none;
  background-color: rgba(0, 0, 0, 0.8);
  top: 0;
  z-index: 10;
  left: 0;
}
.onScroll nav {
  width: 100%;
}
@media screen and (max-width: 1049px) {
  header .phone {
    display: none;
  }
}

@media screen and (max-width: 991px) {
  nav {
    position: relative;
  }
  .navbar-collapse {
    position: absolute;
    top: 0;
    left: 0;
    right: 0;
  }
  .navbar-collapse.show .navbar-nav {
    position: absolute;
    width: 100%;
    top: 104px;
  }
  .nav-item {
    width: 100%;
    background: #fff;
    text-align: center;
  }

  .nav-item:after {
    content: none;
  }
  .nav-item.active .nav-link,
  .nav-item:hover .nav-link {
    color: rgb(248, 96, 17);
  }
  .nav-link {
    padding: 16px 20px !important;
    font-weight: 500;
    font-size: 18px;
    text-align: center;
  }
}
</style>
