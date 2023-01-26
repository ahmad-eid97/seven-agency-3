<template>
  <section class="banner">
    <div class="row m-0 justify-content-center">
      <h2 class="text-center">
        {{ bannerTop.find((one) => one.key === "banner-top_title").value }}
      </h2>
      <div class="heading-spacer">
        <i class="fa-solid fa-angle-down"></i>
      </div>
      <h3>
        {{
          bannerTop.find((one) => one.key === "banner-top_description").value
        }}
      </h3>
      <div class="col text-center">
        <a href="/qoutation" class="btn">Get Qoutation</a>
      </div>
    </div>
  </section>
</template>

<script>
export default {
  name: "AppHomeBanner",
  props: ["bannerTop"],
  data() {
    return {};
  },
  methods: {},
  mounted() {
    document
      .querySelector(".banner")
      .style.setProperty(
        "--bannerTop-bg",
        this.bannerTop.find(
          (one) => one.key === "banner-top_background_active_section"
        ).value === "color"
          ? this.bannerTop.find(
              (one) => one.key === "banner-top_background_color_section"
            ).value
          : `url(${
              this.bannerTop.find(
                (one) => one.key === "banner-top_background_image_section"
              ).value
            })`
      );

    document
      .querySelector(".banner")
      .style.setProperty(
        "--bannerTop-fontSize",
        `${
          this.bannerTop.find(
            (one) => one.key === "banner-top_font_size_section"
          ).value
        }px`
      );

    if (
      this.bannerTop.find(
        (one) => one.key === "banner-top_border_position_section"
      ) &&
      this.bannerTop.find(
        (one) => one.key === "banner-top_border_position_section"
      ).value === "both"
    ) {
      document
        .querySelector(".banner")
        .style.setProperty(
          "--bannerTop-border-top",
          `${
            this.bannerTop.find(
              (one) => one.key === "banner-top_border_size_section"
            ).value
          }px ${
            this.bannerTop.find(
              (one) => one.key === "banner-top_border_type_section"
            ).value
          } ${
            this.bannerTop.find(
              (one) => one.key === "banner-top_border_color_section"
            ).value
          }`
        );

      document
        .querySelector(".banner")
        .style.setProperty(
          "--bannerTop-border-bottom",
          `${
            this.bannerTop.find(
              (one) => one.key === "banner-top_border_size_section"
            ).value
          }px ${
            this.bannerTop.find(
              (one) => one.key === "banner-top_border_type_section"
            ).value
          } ${
            this.bannerTop.find(
              (one) => one.key === "banner-top_border_color_section"
            ).value
          }`
        );
    } else if (
      this.bannerTop.find(
        (one) => one.key === "banner-top_border_position_section"
      ) &&
      this.bannerTop.find(
        (one) => one.key === "banner-top_border_position_section"
      ).value === "top"
    ) {
      document
        .querySelector(".banner")
        .style.setProperty(
          "--bannerTop-border-top",
          `${
            this.bannerTop.find(
              (one) => one.key === "banner-top_border_size_section"
            ).value
          }px ${
            this.bannerTop.find(
              (one) => one.key === "banner-top_border_type_section"
            ).value
          } ${
            this.bannerTop.find(
              (one) => one.key === "banner-top_border_color_section"
            ).value
          }`
        );
    } else if (
      this.bannerTop.find(
        (one) => one.key === "banner-top_border_position_section"
      ) &&
      this.bannerTop.find(
        (one) => one.key === "banner-top_border_position_section"
      ).value === "bottom"
    ) {
      document
        .querySelector(".banner")
        .style.setProperty(
          "--bannerTop-border-bottom",
          `${
            this.bannerTop.find(
              (one) => one.key === "banner-top_border_size_section"
            ).value
          }px ${
            this.bannerTop.find(
              (one) => one.key === "banner-top_border_type_section"
            ).value
          } ${
            this.bannerTop.find(
              (one) => one.key === "banner-top_border_color_section"
            ).value
          }`
        );
    }
  },
};
</script>
<style lang="scss">
.banner {
  /* background-color: rgba(0, 0, 0, 0); */
  /* background-image: -webkit-linear-gradient(
    left,
    rgb(38, 6, 51) 0%,
    rgb(236, 97, 93) 100%
  ); */
  padding: 60px 30px 80px;
  --bannerTop-bg: #fff;
  --bannerTop-fontSize: 20px;
  --bannerTop-border-top: 0px solid #fff;
  --bannerTop-border-bottom: 0px solid #fff;

  background: var(--bannerTop-bg) !important;
  border-top: var(--bannerTop-border-top);
  border-bottom: var(--bannerTop-border-bottom);
  background-repeat: no-repeat;
  background-size: cover;
  h2 {
    font-size: var(--bannerTop-fontSize);
  }
}
.banner h2 {
  color: var(--main-color);
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
  right: 0;
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
@include xs {
  .banner h3 {
    font-size: 32px;
    line-height: 45px;
  }
  .banner .btn {
    border: 3px solid var(--main-color);
    font-size: 15px;
    line-height: 26px;
    width: 250px;
  }
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
</style>
