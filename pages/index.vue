<template>
  <div class="home">
    <app-home-intro></app-home-intro>
    <app-home-who></app-home-who>
    <app-home-why></app-home-why>
    <app-home-banner></app-home-banner>
    <app-home-what></app-home-what>
    <app-home-services></app-home-services>
    <app-home-projects></app-home-projects>
    <app-home-banner-phone></app-home-banner-phone>
    <app-home-owner></app-home-owner>
    <app-home-special></app-home-special>
    <app-home-process></app-home-process>
    <app-home-blogs></app-home-blogs>
    <app-home-contact></app-home-contact>
    <app-home-message></app-home-message>
    <app-home-banner-bottom></app-home-banner-bottom>
  </div>
</template>

<script>
import AppHomeIntro from '../components/home/AppHomeIntro.vue'
import AppHomeWho from '../components/home/AppHomeWho.vue'
import AppHomeWhy from '../components/home/AppHomeWhy.vue'
import AppHomeWhat from '../components/home/AppHomeWhat.vue'
import AppHomeBanner from '../components/home/AppHomeBanner.vue'
import AppHomeBannerPhone from '../components/home/AppHomeBannerPhone.vue'
import AppHomeServices from '../components/home/AppHomeServices.vue'
import AppHomeProjects from '../components/home/AppHomeProjects.vue'
import AppHomeOwner from '../components/home/AppHomeOwner.vue'
import AppHomeSpecial from '../components/home/AppHomeSpecial.vue'
import AppHomeProcess from '../components/home/AppHomeProcess.vue'
import AppHomeBlogs from '../components/home/AppHomeBlogs.vue'
import AppHomeContact from '../components/home/AppHomeContact.vue'
import AppHomeMessage from '../components/home/AppHomeMessage.vue'
import AppHomeBannerBottom from '../components/home/AppHomeBannerBottom.vue'

export default {
  name: 'Home',
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
    AppHomeBannerBottom
  }
}
</script>
<style>
  
</style>