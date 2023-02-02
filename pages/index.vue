<template>
  <div class="home">
    <app-home-intro></app-home-intro>
    <app-home-partners :partners="partners" />
    <div
      v-if="
        $store.state.sectionsStatus.who_we_are &&
        $store.state.sectionsStatus.features
      "
    >
      <app-home-who :whoWeAre="whoWeAre" :features="features"></app-home-who>
    </div>
    <div v-if="$store.state.sectionsStatus.why_choose_us">
      <app-home-why :whyUsSection="whyUsSection"></app-home-why>
    </div>
    <div v-if="$store.state.sectionsStatus.banner - top">
      <app-home-banner :bannerTop="bannerTop"></app-home-banner>
    </div>
    <app-home-what :testimonials="testimonials"></app-home-what>
    <app-home-services :services="services"></app-home-services>
    <app-home-projects :projects="projects"></app-home-projects>
    <app-home-banner-phone></app-home-banner-phone>
    <app-home-owner></app-home-owner>
    <app-home-special :team="team"></app-home-special>
    <div v-if="$store.state.sectionsStatus.process">
      <app-home-process :process="process"></app-home-process>
    </div>
    <div v-if="$store.state.sectionsStatus.activities">
      <app-home-activities :activities="activities" />
    </div>
    <div v-if="$store.state.sectionsStatus.steps">
      <app-home-steps :steps="steps" />
    </div>
    <app-home-blogs :blogs="blogs"></app-home-blogs>
    <app-home-contact></app-home-contact>
    <app-home-message></app-home-message>
    <app-home-banner-bottom></app-home-banner-bottom>
    <SocialChat :attendants="attendants">
      <p slot="header">Click one of our representatives below to chat.</p>
      <template v-slot:button="{ open }">
        <span v-show="!open">Contact us</span>
        <span v-show="open">Close</span>
      </template>
      <small slot="footer">Opening hours: 8am to 10pm</small>
    </SocialChat>
  </div>
</template>

<script>
import AppHomeIntro from "../components/home/AppHomeIntro.vue";
import AppHomeWho from "../components/home/AppHomeWho.vue";
import AppHomeWhy from "../components/home/AppHomeWhy.vue";
import AppHomeWhat from "../components/home/AppHomeWhat.vue";
import AppHomeBanner from "../components/home/AppHomeBanner.vue";
import AppHomeBannerPhone from "../components/home/AppHomeBannerPhone.vue";
import AppHomeServices from "../components/home/AppHomeServices.vue";
import AppHomeProjects from "../components/home/AppHomeProjects.vue";
import AppHomeOwner from "../components/home/AppHomeOwner.vue";
import AppHomeSpecial from "../components/home/AppHomeSpecial.vue";
import AppHomeProcess from "../components/home/AppHomeProcess.vue";
import AppHomeBlogs from "../components/home/AppHomeBlogs.vue";
import AppHomeContact from "../components/home/AppHomeContact.vue";
import AppHomeMessage from "../components/home/AppHomeMessage.vue";
import AppHomeBannerBottom from "../components/home/AppHomeBannerBottom.vue";
import AppHomeActivities from "../components/home/AppHomeActivities.vue";
import AppHomeSteps from "../components/home/AppHomeSteps.vue";
import AppHomePartners from "../components/home/AppHomePartners.vue";

export default {
  name: "Home",
  data() {
    return {
      attendants: [
        {
          app: "whatsapp",
          label: "Support",

          name: this.$store.state.websiteSettings.find(
            (one) => one.key === "chat_widget_whatsapp_label"
          )
            ? this.$store.state.websiteSettings.find(
                (one) => one.key === "chat_widget_whatsapp_label"
              ).plain_value
            : "Laravada",

          number: this.$store.state.websiteSettings.find(
            (one) => one.key === "chat_widget_whatsapp_number"
          )
            ? this.$store.state.websiteSettings.find(
                (one) => one.key === "chat_widget_whatsapp_number"
              ).plain_value
            : "11111111111",

          avatar: {
            src: "https://avatars0.githubusercontent.com/u/8084606?s=460&u=20b6499a416cf7129a18e5c168cf387e159edb1a&v=4",
            alt: "Laravada customer support",
          },
        },
        {
          app: "messenger",
          label: "Technical support",

          name: this.$store.state.websiteSettings.find(
            (one) => one.key === "chat_widget_messenger_label"
          )
            ? this.$store.state.websiteSettings.find(
                (one) => one.key === "chat_widget_messenger_label"
              ).plain_value
            : "Laravada Facebook",

          id: this.$store.state.websiteSettings.find(
            (one) => one.key === "chat_widget_messenger_id"
          )
            ? this.$store.state.websiteSettings.find(
                (one) => one.key === "chat_widget_messenger_id"
              ).plain_value
            : "111111111111",

          avatar: {
            src: "https://avatars0.githubusercontent.com/u/8084606?s=460&u=20b6499a416cf7129a18e5c168cf387e159edb1a&v=4",
            alt: "Laravada customer support",
          },
        },
      ],
    };
  },
  async asyncData({ $axios, app }) {
    const whyUsSection = await $axios.get("/sections/why_choose_us", {
      headers: {
        "Accept-Language": app.i18n.locale,
      },
    });

    const partners = await $axios.get("/partners");

    const features = await $axios.get("/sections/features", {
      headers: {
        "Accept-Language": app.i18n.locale,
      },
    });

    const bannerTop = await $axios.get("/sections/banner-top", {
      headers: {
        "Accept-Language": app.i18n.locale,
      },
    });

    const whoWeAre = await $axios.get("/sections/who_we_are", {
      headers: {
        "Accept-Language": app.i18n.locale,
      },
    });

    const testimonials = await $axios.get("/testimonials");

    // const partners = await $axios.get("/partners");

    const services = await $axios.get("/services");

    const process = await $axios.get("/sections/process", {
      headers: {
        "Accept-Language": app.i18n.locale,
      },
    });

    const projects = await $axios.get("/portfolios");

    const team = await $axios.get("/teams");

    const blogs = await $axios.get("/blogs?latest=1");

    const activities = await $axios.get("/sections/activities", {
      headers: {
        "Accept-Language": app.i18n.locale,
      },
    });

    const steps = await $axios.get("/sections/steps", {
      headers: {
        "Accept-Language": app.i18n.locale,
      },
    });

    return {
      whyUsSection: whyUsSection.data.data,
      partners: partners.data.data.partners,
      bannerTop: bannerTop.data.data,
      features: features.data.data,
      whoWeAre: whoWeAre.data.data,
      testimonials: testimonials.data.data.testimonials,
      services: services.data.data.services,
      process: process.data.data,
      projects: projects.data.data.portfolios,
      team: team.data.data.teams,
      blogs: blogs.data.data.blogs,
      activities: activities.data.data,
      steps: steps.data.data,
    };
  },

  mounted() {
    console.log(this.$store.state.sectionsStatus);
  },
  components: {
    AppHomeIntro,
    AppHomePartners,
    AppHomeWho,
    AppHomeWhy,
    AppHomeBanner,
    AppHomeWhat,
    AppHomeServices,
    AppHomeProjects,
    AppHomeBannerPhone,
    AppHomeOwner,
    AppHomeSpecial,
    AppHomeProcess,
    AppHomeBlogs,
    AppHomeContact,
    AppHomeMessage,
    AppHomeBannerBottom,
    AppHomeActivities,
    AppHomeSteps,
  },
};
</script>
<style>
.home {
  --vsc-bg-header: var(--main-color);
  --vsc-bg-footer: var(--main-color);
  --vsc-text-color-header: #fff;
  --vsc-text-color-footer: #fff;
  --vsc-bg-button: var(--main-color);
  --vsc-text-color-button: #fff;
  --vsc-outline-color: var(--main-color);
  --vsc-border-color-bottom-header: #fff;
  --vsc-border-color-top-footer: #fff;
}
</style>
