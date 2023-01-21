<template>
  <section class="partners specPartners">
    <swiper :options="swiperOption" class="owl-carousel">
      <swiper-slide v-for="partner in partners" :key="partner">
        <div class="item">
          <img class="" :src="partner.image" />
          <h5>{{ partner.title }}</h5>
        </div>
      </swiper-slide>
    </swiper>
  </section>
</template>

<script>
export default {
  name: "AppHomePartners",
  props: ["partners"],
  data() {
    return {
      swiperOption: {
        loop: true,
        slidesPerView: 5,
        spaceBetween: 50,
        breakpoints: {
          // when window width is >= 320px
          100: {
            slidesPerView: 1,
            spaceBetween: 5,
          },
          // when window width is >= 480px
          480: {
            slidesPerView: 2,
            spaceBetween: 5,
          },
          // when window width is >= 640px
          640: {
            slidesPerView: 3,
            spaceBetween: 5,
          },
          992: {
            slidesPerView: 4,
            spaceBetween: 5,
          },
          1200: {
            slidesPerView: 5,
            spaceBetween: 5,
          },
        },
      },
    };
  },
};
</script>
<style lang="scss">
.specPartners {
  margin-top: 30px;
  .swiper-slide {
    display: flex;
    flex-direction: column;
    justify-content: center;
    align-items: center;
  }
}
.partners {
  padding: 0px 100px;
}
.partners .owl-carousel {
  margin-bottom: 40px;
}
.partners .owl-carousel .item {
  text-align: center;
  width: 100px;
}
.partners .owl-carousel .item img {
  height: 100px !important;
  max-width: 100px !important;
  display: inline;
  /* height: auto; */
}
.partners .owl-carousel .item h5 {
  margin-top: 15px;
}
</style>
