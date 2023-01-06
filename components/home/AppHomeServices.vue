<template>
  <section class="services">
    <div
      class="row m-0 justify-content-center content"
      v-if="services.length >= 1"
    >
      <h2 class="text-center">OUR SERVICES</h2>
      <div class="heading-spacer">
        <i class="fa-solid fa-angle-down"></i>
      </div>
      <div
        v-for="service in services.slice(0, 6)"
        :key="service.id"
        class="col-md-6 col-lg-4 mb-4"
      >
        <div class="service">
          <div class="row justify-content-center m-0">
            <div class="col-auto icon">
              <i :class="service.icon"></i>
            </div>
            <h3>{{ service.title }}</h3>
            <p>
              {{ service.description.substring(0, 300) + "..." }}
            </p>
            <hr />
          </div>
        </div>
      </div>
      <div class="servicesBtn">
        <button @click="$router.push('/services')">See All Services</button>
      </div>
    </div>
  </section>
</template>

<script>
export default {
  name: "AppHomeServices",
  props: ["services"],
  data() {
    return {};
  },

  methods: {},
};
</script>
<style lang="scss">
.services {
  background-size: cover;
  background-repeat: no-repeat;
  background-color: rgba(0, 0, 0, 0);
  background-image: url("https://the7.io/agency/wp-content/uploads/sites/43/2017/10/bg003.jpg");
  background-attachment: scroll;
  padding: 60px 30px 80px;
  position: relative;
}
.services::after {
  top: 0;
  bottom: 0;
  left: 0;
  right: 0;
  background-color: rgba(26, 0, 33, 0.9);
  position: absolute;
  content: "";
  z-index: 0;
}
.services .content {
  z-index: 1;
  position: relative;
}
.services h2 {
  color: #ffffff;
  font-weight: 700;
  font-size: 42px;
  line-height: 52px;
}
.services .heading-spacer {
  margin-bottom: 60px;
  position: relative;
  overflow: hidden;
  text-align: center;
}
.services .heading-spacer i {
  color: var(--main-color);
  font-size: 26px;
}
.services .heading-spacer::before {
  content: "";
  position: absolute;
  bottom: 50%;
  right: 0;
  top: 40%;
  width: 60px;
  border-style: solid;
  border-color: #f3615a;
  border-bottom-width: 1px;
  left: 43%;
}
.services .heading-spacer::after {
  content: "";
  position: absolute;
  bottom: 50%;
  right: 0;
  top: 40%;
  width: 60px;
  border-style: solid;
  border-color: #f3615a;
  border-bottom-width: 1px;
  right: 43%;
}
.service {
  border: 2px solid var(--main-color);
  padding: 30px;
  height: 100%;
}
.service.alt {
  border: 2px solid #fff;
  padding: 30px;
  background-color: #fff;
}
.service .icon {
  background: rgba(255, 255, 255, 0.01);
  border: 3px solid var(--main-color);
  width: 66px;
  height: 66px;
  line-height: 66px;
  border-radius: 0px;
  font-size: 30px;
  display: inline-block;
  color: var(--main-color);
  text-align: center;
}
.service h3 {
  color: rgb(255, 255, 255);
  display: block;
  font-size: 26px;
  font-weight: 700;
  line-height: 36px;
  margin-bottom: 15px;
  margin-top: 25px;
  text-align: center;
}
.service.alt h3 {
  color: #000;
}
.service p {
  color: rgb(255, 255, 255);
  display: block;
  font-size: 16px;
  text-align: center;
}
.service.alt p {
  color: rgb(133, 134, 140);
}
.service hr {
  width: 60px;
  margin: 27px 0 0;
  border: 2px solid var(--main-color);
  opacity: 1;
}
.servicesBtn {
  display: flex;
  justify-content: center;
  button {
    border-radius: 0;
    background-color: var(--main-color);
    color: #fff;
    padding: 8px 14px 7px;
  }
}
</style>
