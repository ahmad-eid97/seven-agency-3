<template>
  <div class="home">
    <app-home-intro></app-home-intro>
    <app-home-who :whoWeAre="whoWeAre" :features="features"></app-home-who>
    <app-home-why :whyUsSection="whyUsSection"></app-home-why>
    <app-home-banner :bannerTop="bannerTop"></app-home-banner>
    <app-home-what
      :testimonials="testimonials"
      :partners="partners"
    ></app-home-what>
    <app-home-services :services="services"></app-home-services>
    <app-home-projects :projects="projects"></app-home-projects>
    <app-home-banner-phone></app-home-banner-phone>
    <app-home-owner></app-home-owner>
    <app-home-special :team="team"></app-home-special>
    <app-home-process :process="process"></app-home-process>
    <app-home-blogs :blogs="blogs"></app-home-blogs>
    <app-home-contact></app-home-contact>
    <app-home-message></app-home-message>
    <app-home-banner-bottom></app-home-banner-bottom>
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

export default {
  name: "Home",
  async asyncData({ $axios, app }) {
    const whyUsSection = await $axios.get("/sections/why_choose_us", {
      headers: {
        "Accept-Language": app.i18n.locale,
      },
    });

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

    const partners = await $axios.get("/partners");

    const services = await $axios.get("/services");

    const process = await $axios.get("/sections/process", {
      headers: {
        "Accept-Language": app.i18n.locale,
      },
    });

    const projects = await $axios.get("/portfolios");

    const team = await $axios.get("/teams");

    const blogs = await $axios.get("/blogs?latest=1");

    return {
      whyUsSection: whyUsSection.data.data,
      bannerTop: bannerTop.data.data,
      features: features.data.data,
      whoWeAre: whoWeAre.data.data,
      testimonials: testimonials.data.data.testimonials,
      partners: partners.data.data.partners,
      services: services.data.data.services,
      process: process.data.data,
      projects: projects.data.data.portfolios,
      team: team.data.data.teams,
      blogs: blogs.data.data.blogs,
    };
  },
  components: {
    AppHomeIntro,
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
  },
};
</script>
<style></style>
