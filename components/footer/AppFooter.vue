<template>
  <footer>
    <subscribe />
    <div class="copyrights">
      <div class="row mx-0 align-items-center justify-content-between">
        <div class="col-auto">
          <img
            :src="
              $store.state.websiteSettings.find((one) => one.key === 'logo')
                .plain_value
            "
            alt="logoImage"
            style="width: 200px"
          />
          © 2022 • Laravada • Powered By: Rail Coder
        </div>
        <div class="col-auto">
          <span class="mx-3">
            <span style="color: #d0544e">tel:</span> Call Us:
            {{
              $store.state.websiteSettings.find(
                (one) => one.key === "contact_phone"
              ).plain_value
            }}
          </span>
          <span>
            <span style="color: #d0544e">mail:</span>
            {{
              $store.state.websiteSettings.find((one) => one.key === "email")
                .plain_value
            }}
          </span>
        </div>
      </div>
    </div>
  </footer>
</template>

<script>
import Subscribe from "../subscribe/subscribe.vue";
export default {
  name: "AppFooter",
  components: { Subscribe },
  data() {
    return {};
  },
  methods: {},
};
</script>
<style>
footer {
  /* margin-top: 50px; */
}
.copyrights {
  padding: 15px 30px;
  margin-bottom: 0px;
  background-color: rgb(17, 17, 17);
  color: rgb(255, 255, 255);
  font-size: 13px;
  letter-spacing: normal;
  line-height: 23px;
}
.copyrights p a {
  color: rgb(166, 166, 166);
  font-size: 12px;
  font-weight: 600;
  text-decoration: none;
}
</style>
