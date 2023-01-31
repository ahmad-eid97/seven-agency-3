<template>
  <section class="process">
    <div class="row m-0 justify-content-center content">
      <h2 class="text-center">
        {{ process.find((one) => one.key === "process_title").value }}
      </h2>
      <div class="heading-spacer">
        <i class="fa-solid fa-angle-down"></i>
      </div>
      <div class="icons">
        <ul class="icon_list top">
          <div
            class="row justify-content-center"
            v-if="process.find((one) => one.key === 'process_list').value"
          >
            <div
              v-for="item in process
                .find((one) => one.key === 'process_list')
                .value.slice(0, 2)"
              :key="item"
              class="col-6 square"
            >
              <li class="icon_list_item">
                <div class="icon_list_icon">
                  <i :class="item.icon"></i>
                </div>
                <h3>{{ item.number }}.</h3>
                <div
                  class="icon_list_connector"
                  :class="$i18n.locale === 'ar' ? 'arabic' : ''"
                ></div>
              </li>
            </div>
          </div>
        </ul>
      </div>
      <div
        class="row m-0 justify-content-center"
        v-if="process.find((one) => one.key === 'process_list').value"
      >
        <div
          v-for="item in process
            .find((one) => one.key === 'process_list')
            .value.slice(0, 2)"
          :key="item"
          class="col-lg-6 text"
        >
          <h3>{{ item.title }}</h3>
          <p>
            {{ item.description }}
          </p>
        </div>
      </div>
      <div class="icons">
        <ul
          class="icon_list top"
          v-if="process.find((one) => one.key === 'process_list').value"
        >
          <div class="row"></div>

          <li
            v-for="item in process
              .find((one) => one.key === 'process_list')
              .value.slice(
                2,
                process.find((one) => one.key === 'process_list').value.length
              )"
            :key="item"
            class="icon_list_item squareTwo"
          >
            <div class="icon_list_icon">
              <i :class="item.icon"></i>
            </div>

            <h3>{{ item.number }}.</h3>

            <div
              class="icon_list_connector"
              :class="$i18n.locale === 'ar' ? 'arabic' : ''"
            ></div>
          </li>
        </ul>
      </div>
      <div
        class="row m-0 justify-content-center"
        v-if="process.find((one) => one.key === 'process_list').value"
      >
        <div
          v-for="item in process
            .find((one) => one.key === 'process_list')
            .value.slice(
              2,
              process.find((one) => one.key === 'process_list').value.length
            )"
          :key="item"
          class="col-lg-4 text"
        >
          <h3>{{ item.title }}</h3>
          <p>
            {{ item.description }}
          </p>
        </div>
      </div>
    </div>
  </section>
</template>

<script>
export default {
  name: "AppHomeProcess",
  props: ["process"],
  data() {
    return {};
  },
  methods: {},
  mounted() {
    document
      .querySelector(".process")
      .style.setProperty(
        "--process-bg",
        this.process.find(
          (one) => one.key === "process_background_active_section"
        ).value === "color"
          ? this.process.find(
              (one) => one.key === "process_background_color_section"
            ).value
          : `url(${
              this.process.find(
                (one) => one.key === "process_background_image_section"
              ).value
            })`
      );

    document
      .querySelector(".process")
      .style.setProperty(
        "--process-fontSize",
        `${
          this.process.find((one) => one.key === "process_font_size_section")
            .value
        }px`
      );

    if (
      this.process.find(
        (one) => one.key === "process_border_position_section"
      ) &&
      this.process.find((one) => one.key === "process_border_position_section")
        .value === "both"
    ) {
      document
        .querySelector(".process")
        .style.setProperty(
          "--process-border-top",
          `${
            this.process.find(
              (one) => one.key === "process_border_size_section"
            ).value
          }px ${
            this.process.find(
              (one) => one.key === "process_border_type_section"
            ).value
          } ${
            this.process.find(
              (one) => one.key === "process_border_color_section"
            ).value
          }`
        );

      document
        .querySelector(".process")
        .style.setProperty(
          "--process-border-bottom",
          `${
            this.process.find(
              (one) => one.key === "process_border_size_section"
            ).value
          }px ${
            this.process.find(
              (one) => one.key === "process_border_type_section"
            ).value
          } ${
            this.process.find(
              (one) => one.key === "process_border_color_section"
            ).value
          }`
        );
    } else if (
      this.process.find(
        (one) => one.key === "process_border_position_section"
      ) &&
      this.process.find((one) => one.key === "process_border_position_section")
        .value === "top"
    ) {
      document
        .querySelector(".process")
        .style.setProperty(
          "--process-border-top",
          `${
            this.process.find(
              (one) => one.key === "process_border_size_section"
            ).value
          }px ${
            this.process.find(
              (one) => one.key === "process_border_type_section"
            ).value
          } ${
            this.process.find(
              (one) => one.key === "process_border_color_section"
            ).value
          }`
        );
    } else if (
      this.process.find(
        (one) => one.key === "process_border_position_section"
      ) &&
      this.process.find((one) => one.key === "process_border_position_section")
        .value === "bottom"
    ) {
      document
        .querySelector(".process")
        .style.setProperty(
          "--process-border-bottom",
          `${
            this.process.find(
              (one) => one.key === "process_border_size_section"
            ).value
          }px ${
            this.process.find(
              (one) => one.key === "process_border_type_section"
            ).value
          } ${
            this.process.find(
              (one) => one.key === "process_border_color_section"
            ).value
          }`
        );
    }
  },
};
</script>
<style lang="scss">
.process {
  background-size: cover;
  background-repeat: no-repeat;
  background-color: rgba(0, 0, 0, 0);
  /* background-image: url("https://the7.io/agency/wp-content/uploads/sites/43/2017/10/bg003.jpg"); */
  background-attachment: scroll;
  padding: 60px 30px 80px;
  position: relative;
  text-align: center;
  --process-bg: #fff;
  --process-fontSize: 20px;
  --process-border-top: 0px solid #fff;
  --process-border-bottom: 0px solid #fff;

  background: var(--process-bg) !important;
  border-top: var(--process-border-top);
  border-bottom: var(--process-border-bottom);
  h2 {
    font-size: var(--process-fontSize);
  }
}
.process::after {
  top: 0;
  bottom: 0;
  left: 0;
  right: 0;
  background-color: rgba(26, 0, 33, 0.9);
  position: absolute;
  content: "";
  z-index: 0;
}
.process .content {
  z-index: 1;
  position: relative;
}
.process h2 {
  color: #ffffff;
  font-weight: 700;
  font-size: 42px;
  line-height: 52px;
}
@include md {
  .icon_list_connector {
    display: none;
  }
}
.process .heading-spacer {
  margin-bottom: 60px;
  position: relative;
  overflow: hidden;
  text-align: center;
}
.process .heading-spacer i {
  color: var(--main-color);
  font-size: 26px;
}
.process .heading-spacer::before {
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
.process .heading-spacer::after {
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
.process .icons {
  padding: 25px 25px 0;
}
.process ul {
  list-style: none;
  justify-content: center;
  display: flex;
}
.process .icon_list_item {
  // width: 385px;
  position: relative;
  display: table-cell;
  @include xs {
    width: 100px;
  }
}
.square:nth-of-type(2) {
  .icon_list_connector {
    display: none;
  }
}
.squareTwo:nth-of-type(3) {
  .icon_list_connector {
    display: none;
  }
}
.process .icon_list_icon {
  background-color: var(--main-color);
  border-bottom-color: var(--main-color);
  border-bottom-style: solid;
  border-bottom-width: 3px;
  border-left-color: var(--main-color);
  border-left-style: solid;
  border-left-width: 3px;
  border-right-color: var(--main-color);
  border-right-style: solid;
  border-right-width: 3px;
  border-top-color: var(--main-color);
  border-top-style: solid;
  border-top-width: 3px;
  box-sizing: content-box;
  color: rgb(255, 255, 255);
  font-size: 30px;
  height: 90px;
  line-height: 90px;
  margin-bottom: 0px;
  margin-left: 144.5px;
  margin-right: 144.5px;
  margin-top: 0px;
  padding-bottom: 0px;
  padding-left: 0px;
  padding-right: 0px;
  padding-top: 0px;
  position: relative;
  text-align: center;
  width: 90px;
  z-index: 9;
}
ul {
  padding: 0 !important;
}
@include md {
  .process .icon_list_icon {
    margin-left: 10px;
    margin-right: 10px;
  }
}
.icon_list_item h3 {
  margin: 15px;
  color: var(--main-color);
  font-size: 26px;
  font-weight: 700;
  line-height: 26px;
  text-align: center;
}
.icon_list_item .icon_list_connector {
  border: 1px dashed var(--main-color);
  position: absolute;
  text-transform: none;
  top: 45px;
  width: 385px;
  left: 192.5px;
  &.arabic {
    left: unset;
    right: 192.5px;
  }
}
.process .text {
  width: 385px;
}
.process .text h3 {
  color: rgb(255, 255, 255);
  font-size: 26px;
  font-weight: 700;
  line-height: 36px;
  margin-bottom: 16px;
}
.process .text p {
  color: rgb(255, 255, 255);
  font-size: 16px;
  font-weight: 400;
  line-height: 28px;
}
</style>
