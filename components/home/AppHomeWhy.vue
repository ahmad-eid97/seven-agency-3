<template>
  <section class="why">
    <div class="row m-0">
      <div class="col-lg-6 text">
        <div class="row m-0">
          <h1 class="text-center">
            {{
              whyUsSection.find((one) => one.key === "why_choose_us_title")
                .value
            }}
          </h1>
          <div class="heading-spacer">
            <i class="fa-solid fa-angle-down"></i>
          </div>
          <p>
            {{
              whyUsSection.find(
                (one) => one.key === "why_choose_us_description"
              ).value
            }}
          </p>
        </div>
        <div class="row m-0">
          <div
            class="items"
            v-if="
              whyUsSection.find((one) => one.key === 'why_choose_us_list').value
            "
          >
            <div
              v-for="item in whyUsSection.find(
                (one) => one.key === 'why_choose_us_list'
              ).value"
              :key="item"
              class="item"
            >
              <div class="row m-0">
                <div class="col-auto icon">
                  <i :class="item.icon"></i>
                </div>
                <div class="col item-text">
                  <h3>{{ item.title }}</h3>
                  <p>
                    {{ item.description }}
                  </p>
                </div>
              </div>
            </div>
          </div>
        </div>
      </div>
      <div
        class="col-lg-6 image"
        :style="{
          backgroundImage: whyUsSection.find(
            (one) => one.key === 'why_choose_us_image'
          ).value,
        }"
      >
        <img
          :src="
            whyUsSection.find((one) => one.key === 'why_choose_us_image').value
          "
          alt=""
        />
      </div>
    </div>
  </section>
</template>

<script>
export default {
  name: "AppHomeWhy",
  props: ["whyUsSection"],
  data() {
    return {};
  },

  methods: {},
};
</script>
<style lang="scss">
.why {
  padding: 0;
}
.why h1 {
  color: rgb(51, 51, 51);
  font-size: 42px;
  font-weight: 700;
  line-height: 52px;
}
.why .heading-spacer {
  margin-bottom: 60px;
  position: relative;
  overflow: hidden;
  text-align: center;
}
.why .heading-spacer i {
  color: var(--main-color);
  font-size: 26px;
}
.why .heading-spacer::before {
  content: "";
  position: absolute;
  bottom: 50%;
  right: 0;
  top: 40%;
  width: 60px;
  border-style: solid;
  border-color: #f3615a;
  border-bottom-width: 1px;
  left: 36%;
}
.why .heading-spacer::after {
  content: "";
  position: absolute;
  bottom: 50%;
  right: 0;
  top: 40%;
  width: 60px;
  border-style: solid;
  border-color: #f3615a;
  border-bottom-width: 1px;
  right: 36%;
}
.why .text {
  background-color: #f7f7f7;
  padding: 80px 5% 60px;
}
.why .text p {
  color: rgb(133, 134, 140);
  font-size: 16px;
  font-weight: 400;
  line-height: 26px;
  padding-bottom: 35px;
  text-align: center;
}
.why .text .btn {
  color: rgb(255, 255, 255);
  font-size: 13px;
  margin-bottom: 10px;
  margin-right: 10px;
  padding-bottom: 7px;
  padding-left: 14px;
  padding-right: 14px;
  padding-top: 8px;
  text-align: center;
  background-color: #f3615a;
  border-radius: 0;
  width: 180px;
  font-weight: 700;
  text-transform: uppercase;
}
.why .image {
  /* padding-top: 150px !important;
    padding-bottom: 150px !important;
    background-image: url(https://the7.io/agency/wp-content/uploads/sites/43/2017/10/bg001.jpg?id=631) !important;
    background-position: center !important;
    background-repeat: no-repeat !important;
    background-size: cover !important; */
  img {
    width: 100%;
    height: 100%;
  }
}

.why .item .icon {
  background: rgba(255, 255, 255, 0.01);
  border: 3px solid var(--main-color);
  width: 60px;
  height: 60px;
  line-height: 60px;
  border-radius: 0px;
  font-size: 24px;
  display: inline-block;
  color: var(--main-color);
  text-align: center;
}
.why .item .item-text h3 {
  color: rgb(51, 51, 51);
  font-size: 20px;
  line-height: 30px;
  margin: 0;
}
.why .item .item-text p {
  color: rgb(133, 134, 140);
  float: left;
  font-size: 16px;
  margin-top: 10px;
  margin-bottom: 0;
}
</style>
