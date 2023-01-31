<template>
  <section class="banner customBanner">
    <div class="row m-0 justify-content-center">
      <h2 class="text-center">Check Out Our Social Links!</h2>
      <div class="heading-spacer">
        <i class="fa-solid fa-angle-down"></i>
      </div>
    </div>
    <div class="row justify-content-center">
      <div class="col-auto text-center">
        <div class="social-bottom">
          <a
            :href="`https://${$store.state.footerData.youtube}`"
            target="_blank"
          >
            <i class="fa-brands fa-youtube"></i>
          </a>
          <p>Youtube</p>
        </div>
      </div>
      <div class="col-auto text-center">
        <div class="social-bottom">
          <a
            :href="`https://${$store.state.footerData.instagram}`"
            target="_blank"
          >
            <i class="fa-brands fa-instagram"></i>
          </a>
          <p>Instagram</p>
        </div>
      </div>
      <div class="col-auto text-center">
        <div class="social-bottom">
          <a
            :href="`https://${$store.state.footerData.facebook}`"
            target="_blank"
          >
            <i class="fa-brands fa-facebook-f"></i>
          </a>
          <p>Facebook</p>
        </div>
      </div>
      <div class="col-auto text-center">
        <div class="social-bottom">
          <a
            :href="`https://${$store.state.footerData.linkedin}`"
            target="_blank"
          >
            <i class="fa-brands fa-linkedin-in"></i>
          </a>
          <p>Linkedin</p>
        </div>
      </div>
    </div>
  </section>
</template>

<script>
export default {
  name: "AppHomeBanner",
  data() {
    return {};
  },

  methods: {},
};
</script>
<style lang="css">
.customBanner {
  background-color: rgba(0, 0, 0, 0);
  background-image: -webkit-linear-gradient(
    left,
    rgb(38, 6, 51) 0%,
    rgb(236, 97, 93) 100%
  ) !important;
}
.banner {
  padding: 60px 30px 80px;
}
.banner h2 {
  color: #fff;
  font-weight: 700;
  font-size: 26px;
  line-height: 36px;
}
.banner .heading-spacer {
  margin-bottom: 60px;
  position: relative;
  overflow: hidden;
  text-align: center;
}
.banner .heading-spacer i {
  color: var(--main-color);
  font-size: 26px;
}
.banner .heading-spacer::before {
  content: "";
  position: absolute;
  bottom: 50%;
  /* right: 0; */
  top: 40%;
  width: 60px;
  border-style: solid;
  border-color: var(--main-color);
  border-bottom-width: 1px;
  left: 43%;
}
.banner .heading-spacer::after {
  content: "";
  position: absolute;
  bottom: 50%;
  right: 0;
  top: 40%;
  width: 60px;
  border-style: solid;
  border-color: var(--main-color);
  border-bottom-width: 1px;
  right: 43%;
}
.banner h3 {
  margin-bottom: 40px;
  color: rgb(255, 255, 255);
  font-size: 42px;
  font-weight: 700;
  letter-spacing: normal;
  line-height: 52px;
  margin-bottom: 40px;
  text-align: center;
}
.banner .btn {
  border: 3px solid var(--main-color);
  border-radius: 0;
  font-size: 26px;
  font-weight: 700;
  line-height: 26px;
  padding: 16px 30px;
  height: 64px;
  width: 500px;
  color: #fff;
}
.banner .btn:hover {
  border: 3px solid #fff;
  border-radius: 0;
  font-size: 26px;
  font-weight: 700;
  line-height: 26px;
  padding: 16px 30px;
  height: 64px;
  width: 500px;
  background: #fff;
  color: var(--main-color);
}
.banner .social-bottom {
  margin: 0 30px;
}
.banner .social-bottom p {
  color: #fff;
  margin: 25px 0 15px;
  font-size: 16px;
  line-height: 18px;
  font-weight: 700;
}
.banner .social-bottom a {
  color: #ffffff;
  background: var(--main-color);
  width: 70px;
  height: 70px;
  line-height: 70px;
  border-radius: 500px;
  font-size: 30px;
  display: block;
  transition: all 0.3s linear;
}
.banner .social-bottom a:hover {
  transform: scale(1.2);
}
</style>
