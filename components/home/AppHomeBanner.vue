<template>
    <section class="banner">
        <div class="row m-0 justify-content-center">
            <h2 class="text-center">Limited Time Offer!</h2>
            <div class="heading-spacer">
                <font-awesome-icon icon="fa-solid fa-angle-down" />
            </div>
            <h3>
                Hurry up! Contact us today ang get 100% free first online consultation!
            </h3>
            <div class="col text-center">
                <a href="#" class="btn">GET FREE CONSULTATION</a>
            </div>
        </div>
    </section>
</template>

<script>
export default {
    name: 'AppHomeBanner',
    data() {
        return {
           
        }
    },
    
    methods: {
        
    }
}
</script>
<style lang="scss">
    .banner {
        background-color: rgba(0, 0, 0, 0);
        background-image: -webkit-linear-gradient(left, rgb(38, 6, 51) 0%, rgb(236, 97, 93) 100%);
        padding: 60px 30px 80px;
    }
    .banner h2 {
        color: var(--main-color);
        font-weight: 700;
        font-size: 26px;
        line-height: 36px;
    }
    .banner .heading-spacer {
        margin-bottom: 60px;
        height: 21px;
        position: relative;
        overflow: hidden;
        text-align: center;
    }
    .banner .heading-spacer svg {
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
        border-color: #f3615a;
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
        border-color: #f3615a;
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