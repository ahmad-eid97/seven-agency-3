<template>
    <div class="home">
        <app-faq-heading></app-faq-heading>
        <app-faq-faqs :faqs="faqs"></app-faq-faqs>
    </div>
</template>

<script>
import AppFaqFaqs from '../../components/faq/AppFaqFaqs.vue'
import AppFaqHeading from '../../components/faq/AppFaqHeading.vue'
export default {
  components: { AppFaqHeading, AppFaqFaqs },
  name: 'Faq',
  async asyncData({ $axios }) {
    return await $axios.get('/faqs').then(res => {
      return {
        faqs: res.data.data
      }
    });
  },
}
</script>

<style>

</style>