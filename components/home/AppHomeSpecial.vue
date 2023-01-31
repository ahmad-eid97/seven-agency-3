<template>
  <section class="special">
    <div class="row m-0 justify-content-center">
      <h1 class="text-center">OUR SPECIALISTS</h1>
      <div class="heading-spacer">
        <i class="fa-solid fa-angle-down"></i>
      </div>
    </div>
    <div class="row special-carousel">
      <swiper
        :options="swiperOption"
        class="owl-carousel"
        v-if="team.length >= 1"
      >
        <swiper-slide v-for="member in team" :key="member.id">
          <div class="item">
            <div class="row m-0 justify-content-center">
              <div class="col-auto user">
                <img :src="member.image" :alt="member.name" />
              </div>
              <div class="col-12 text">
                <h3>{{ member.name }}</h3>
                <h4>
                  {{ member.job }}
                </h4>
                <p>
                  {{ member.description }}
                </p>
                <div href="#" class="social-owner">
                  <a href="#">
                    <i class="fa-brands fa-behance"></i>
                  </a>
                  <a href="#">
                    <i class="fa-brands fa-instagram"></i>
                  </a>
                  <a href="#">
                    <i class="fa-brands fa-facebook-f"></i>
                  </a>
                  <a href="#">
                    <i class="fa-brands fa-twitter"></i>
                  </a>
                </div>
              </div>
            </div>
          </div>
        </swiper-slide>
      </swiper>
    </div>
  </section>
</template>

<script>
export default {
  name: "AppHomeSpecial",
  props: ["team"],
  data() {
    return {
      swiperOption: {
        loop: true,
        slidesPerView: 3,
        spaceBetween: 50,
        breakpoints: {
          // when window width is >= 320px
          100: {
            slidesPerView: 1,
            spaceBetween: 5,
          },
          // when window width is >= 480px
          480: {
            slidesPerView: 1,
            spaceBetween: 5,
          },
          // when window width is >= 640px
          640: {
            slidesPerView: 2,
            spaceBetween: 5,
          },
          992: {
            slidesPerView: 2,
            spaceBetween: 5,
          },
          1200: {
            slidesPerView: 3,
            spaceBetween: 5,
          },
        },
      },
    };
  },

  methods: {},
};
</script>
<style lang="css">
.special {
  padding: 80px 50px 100px;
}
.special h1 {
  color: rgb(51, 51, 51);
  font-size: 42px;
  font-weight: 700;
  line-height: 52px;
}
.special .heading-spacer {
  margin-bottom: 60px;
  position: relative;
  overflow: hidden;
  text-align: center;
}
.special .heading-spacer i {
  color: var(--main-color);
  font-size: 26px;
}
.special .heading-spacer::before {
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
.special .heading-spacer::after {
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
.special .item {
  padding: 20px 0 30px;
}
.special .item .user {
  width: 140px;
  height: 140px;
  border-radius: 50%;
  overflow: hidden;
  padding: 0;
}
.special .item .text {
  text-align: center;
}
.special .item .text h3 {
  font-size: 20px;
  font-weight: 700;
  letter-spacing: normal;
  line-height: 30px;
  color: rgb(51, 51, 51);
}
.special .item .text h4 {
  color: var(--main-color);
  font-size: 16px;
  font-weight: 700;
  letter-spacing: normal;
  line-height: 28px;
}
.special .item .text p {
  color: rgb(133, 134, 140);
  font-size: 16px;
  font-style: italic;
  letter-spacing: normal;
  line-height: 26px;
  margin-bottom: 10px;
}
.special .social-owner {
  display: flex;
  justify-content: center;
}
.special .social-owner a {
  color: var(--main-color);
  display: inline-flex;
  font-size: 16px;
  height: 28px;
  justify-content: center;
  line-height: 28px;
  margin-right: 5px;
  position: relative;
  text-align: center;
  text-decoration-color: var(--main-color);
  text-decoration-line: none;
  width: 28px;
  border: 2px solid transparent;
  border-radius: 100px;
  align-items: center;
  transition: all 0.15s linear;
}
.special .social-owner a:hover {
  background-color: var(--main-color);
  color: #fff;
}
</style>
