<template>
    <section class="banner phone">
        <div class="row m-0 justify-content-center align-items-center">
           <div class="col-auto">
               <h3>Have a project for us? Call us now!</h3>
           </div>
           <div class="col-auto">
               <p>
                   <font-awesome-icon icon="fa-solid fa-square-phone" />
                    001 234 56 78
               </p>
           </div>
        </div>
    </section>
</template>

<script>
export default {
    name: 'AppHomeBannerPhone',
    data() {
        return {
           
        }
    },
    
    methods: {
        
    }
}
</script>
<style lang="css">
    .banner {
        background-color: rgba(0, 0, 0, 0);
        background-image: -webkit-linear-gradient(left, rgb(38, 6, 51) 0%, rgb(236, 97, 93) 100%);
        padding: 50px 0 40px;
    }
    
    .banner.phone h3 {
        color: var(--main-color);
        display: inline-block;
        font-size: 26px;
        font-weight: 700;
        letter-spacing: normal;
        line-height: 36px;
        margin: 0;
    }
    .banner.phone p {
        color: rgb(255, 255, 255);
        display: block;
        font-size: 48px;
        font-weight: 700;
        letter-spacing: normal;
        line-height: 58px;
        margin: 0;
    }
</style>