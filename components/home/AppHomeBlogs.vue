<template>
  <section class="blogs">
    <div class="row m-0 justify-content-center">
      <h1 class="text-center">FROM OUR BLOG</h1>
      <div class="heading-spacer">
        <i class="fa-solid fa-angle-down"></i>
      </div>
    </div>
    <div class="row blogs-carousel">
      <swiper
        :options="swiperOption"
        class="owl-carousel"
        v-if="blogs.length >= 1"
      >
        <swiper-slide v-for="blog in blogs" :key="blog.id">
          <div class="item">
            <div class="row m-0 justify-content-center">
              <div class="image">
                <img class="img-fluid" :src="blog.image" :alt="blog.title" />
                <span class="tag">Events</span>
                <span class="date"
                  ><span class="month">{{
                    $date(new Date(blog.publish_date), "MMM")
                  }}</span
                  ><span class="day">{{
                    $date(new Date(blog.publish_date), "dd")
                  }}</span
                  ><span class="year">{{
                    $date(new Date(blog.publish_date), "yyyy")
                  }}</span></span
                >
              </div>
              <div class="col-12 text">
                <h3>{{ blog.title }}</h3>

                <p>
                  {{ blog.description.substring(0, 250) + "..." }}
                </p>
                <div href="#" class="btns">
                  <nuxt-link :to="`/blog/${blog.id}`" class="btn">
                    Read article
                    <i class="fa-solid fa-caret-right"></i>
                  </nuxt-link>
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
  name: "AppHomeblogs",
  props: ["blogs"],
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
<style lang="scss">
.blogs {
  padding: 80px 50px 100px;
}
@include xs {
  .blogs {
    padding: 50px 20px 50px;
  }
}
.blogs h1 {
  color: rgb(51, 51, 51);
  font-size: 42px;
  font-weight: 700;
  line-height: 52px;
}
.blogs .heading-spacer {
  margin-bottom: 60px;
  position: relative;
  overflow: hidden;
  text-align: center;
}
.blogs .heading-spacer i {
  color: var(--main-color);
  font-size: 26px;
}
.blogs .heading-spacer::before {
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
.blogs .heading-spacer::after {
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
.blogs .item {
  padding: 20px 10px 30px;
}
.blogs .item .image {
  overflow: hidden;
  padding: 0;
  position: relative;
}
.blogs .item .image img {
  transition: all 2s linear;
  height: 300px;
  width: 100% !important;
}
.blogs .item .image:hover img {
  transform: scale(1.3);
}
.blogs .item .tag {
  padding: 2px 9px 1px;
  margin: 0 0 2px;
  text-decoration: none;
  background-color: rgba(0, 0, 0, 0.75);
  color: #fff;
  top: 10px;
  position: absolute;
  left: 10px;
}
.blogs .item .date {
  position: absolute;
  top: 10px;
  right: 10px;
  z-index: 30;
  background: #fff;
  min-height: 80px;
  min-width: 42px;
  padding: 2px 0;
}
.blogs .item .date span {
  display: block;
  text-align: center;
  position: relative;
}
.blogs .item .date .month {
  font-size: 12px;
  font-weight: 700;
  line-height: 22px;
  margin-bottom: 2px;
}
.blogs .item .date .month:after {
  background-color: var(--main-color);
  bottom: -2px;
  height: 2px;
  content: "";
  position: absolute;
  width: 14px;
  left: 14px;
}
.blogs .item .date .day {
  font-size: 22px;
  font-weight: 700;
  line-height: 22px;
  margin-bottom: 2px;
  padding: 3px;
}
.blogs .item .date .day:after {
  background-color: var(--main-color);
  bottom: -2px;
  height: 2px;
  content: "";
  position: absolute;
  width: 14px;
  left: 14px;
}
.blogs .item .date .year {
  font-size: 12px;
  font-weight: 700;
  line-height: 22px;
  margin-bottom: 2px;
}
.blogs .item .text {
  text-align: start;
  padding-top: 25px;
}
.blogs .item .text h3 {
  font-size: 20px;
  font-weight: 700;
  letter-spacing: normal;
  line-height: 30px;
  color: rgb(51, 51, 51);
}

.blogs .item .text p {
  color: rgb(133, 134, 140);
  font-size: 16px;
  line-height: 28px;
  margin-bottom: 10px;
}
.blogs .btn {
  border-radius: 0;
  background-color: var(--main-color);
  color: #fff;
  padding: 8px 14px 7px;
}
</style>
