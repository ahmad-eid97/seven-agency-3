<template>
  <div id="app" :class="$i18n.locale === 'en' ? 'english' : 'arabic'">
    <Loader v-if="$store.state.showLoader" />
    <!-- <app-header ></app-header> -->

    <router-view />
    <div class="cart" :class="openCart ? 'opened' : ''">
      <div class="head">
        <i class="fa-regular fa-xmark" @click="openCart = false"></i>
        <button
          @click="goToCheckout"
          :disabled="$store.state.cartItems.length <= 0"
        >
          <i class="fa-regular fa-badge-check"></i> Checkout
        </button>
      </div>
      <cart />
    </div>
    <div class="m-0 cartIcon" @click="openCart = !openCart">
      <span>{{ $store.state.cartItems.length }}</span>
      <i class="fa-regular fa-cart-plus"></i>
    </div>

    <app-footer></app-footer>
  </div>
</template>

<script>
import Loader from "../components/UIs/Loader.vue";
import cart from "../components/cart/cart.vue";
// import AppHeader from '../components/header/AppHeader.vue'
import AppFooter from "../components/footer/AppFooter.vue";

export default {
  name: "App",
  components: {
    // AppHeader,
    AppFooter,
    cart,
    Loader,
  },
  data() {
    return {
      openCart: false,
    };
  },
  watch: {
    $route(to, from) {
      window.scrollTo(0, 0);
    },
  },
  methods: {
    goToCheckout() {
      this.openCart = false;
      this.$router.push("/checkout");
    },
  },

  created() {
    // this.$route.params.lang = localStorage.getItem('code');
    // if (this.$route.params.lang === 'ar') {
    //   localStorage.setItem('code', 'ar');
    //   this.$i18n.locale = 'ar';
    //   document.documentElement.setAttribute('dir', 'rtl');
    //   document.documentElement.setAttribute('lang', 'ar');
    //   document.body.classList.add('rtl');
    // } else {
    //   localStorage.setItem('code', 'en');
    //   this.$i18n.locale = 'en';
    //   document.documentElement.setAttribute('dir', 'ltr');
    //   document.documentElement.setAttribute('lang', 'en');
    //   document.body.classList.remove('rtl');
    // }
  },
  mounted() {
    // this.$route.params.lang  = this.lang;
    this.$store.state.cartItems = localStorage.getItem("laravadaCart")
      ? JSON.parse(localStorage.getItem("laravadaCart"))
      : [];

    document
      .querySelector(":root")
      .style.setProperty(
        "--main-color",
        this.$store.state.websiteSettings.find(
          (one) => one.key === "primary_color"
        ).plain_value
      );

    // document
    //   .querySelector(":root")
    //   .style.setProperty(
    //     "--secondary-color",
    //     this.$store.state.websiteSettings.find(
    //       (one) => one.key === "secondary_color"
    //     ).plain_value
    //   );
  },
};
</script>
<style lang="scss">
.cart {
  width: 390px;
  height: 100vh;
  position: fixed;
  top: 0;
  right: 0;
  transform: translateX(390px);
  background-color: #fff;
  z-index: 99999;
  box-shadow: 2px 2px 10px rgba(0, 0, 0, 0.2);
  .head {
    display: flex;
    align-items: center;
    justify-content: space-between;
    padding: 10px;
    & > i {
      border: 1px solid var(--main-color);
      border-radius: 5px;
      width: 30px;
      height: 30px;
      display: grid;
      place-items: center;
      cursor: pointer;
      background-color: var(--main-color);
      color: #fff;
      &:hover {
        color: var(--main-color);
        background: transparent;
      }
    }
    button {
      padding: 5px 30px;
      font-size: 1.1rem;
      background-color: var(--main-color);
      color: #fff;
      border: 1px solid var(--main-color);
      display: flex;
      align-items: center;
      gap: 5px;
      i {
        font-size: 1.1rem;
      }
      &:disabled {
        opacity: 0.5;
        cursor: not-allowed;
        &:hover {
          background-color: var(--main-color);
          color: #fff;
        }
      }
      &:hover {
        background-color: transparent;
        color: var(--main-color);
      }
    }
  }
  &.opened {
    transform: translateX(0);
  }
  @include xs {
    width: 350px;
  }
}
.cartIcon {
  border: 1px solid var(--main-color);
  border-radius: 5px;
  width: 45px;
  height: 45px;
  display: grid;
  place-items: center;
  cursor: pointer;
  position: fixed;
  top: 90px;
  right: 20px;
  z-index: 999;
  background-color: #fff;
  span {
    position: absolute;
    top: -15px;
    right: -10px;
    width: 30px;
    height: 30px;
    background-color: var(--main-color);
    border-radius: 50%;
    color: #fff;
    display: grid;
    place-content: center;
    font-size: 1.2rem;
  }
  i {
    color: var(--main-color);
  }
  &:hover {
    background-color: var(--main-color);
    border-color: var(--main-color);
    i {
      color: #fff;
    }
  }
}
</style>
