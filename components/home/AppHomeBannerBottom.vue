<template>
    <section class="banner">
        <div class="row m-0 justify-content-center">
            <h2 class="text-center">Check Out Our Social Links!</h2>
            <div class="heading-spacer">
                <font-awesome-icon icon="fa-solid fa-angle-down" />
            </div>
        </div>
        <div class="row justify-content-center">
            <div class="col-auto  text-center">
                <div class="social-bottom">
                    <a href="#">
                        <font-awesome-icon icon="fa-brands fa-twitter" />
                    </a>
                    <p>
                        Twitter
                    </p>
                </div>
            </div>
            <div class="col-auto  text-center">
                <div class="social-bottom">
                    <a href="#">
                        <font-awesome-icon icon="fa-brands fa-pinterest-p" />
                    </a>
                    <p>
                        Pinterest
                    </p>
                </div>
            </div>
            <div class="col-auto  text-center">
                <div class="social-bottom">
                    <a href="#">
                        <font-awesome-icon icon="fa-brands fa-facebook-f" />
                    </a>
                    <p>
                        Facebook
                    </p>
                </div>
            </div>
            <div class="col-auto  text-center">
                <div class="social-bottom">
                    <a href="#">
                        <font-awesome-icon icon="fa-brands fa-behance" />
                    </a>
                    <p>
                        Behance
                    </p>
                </div>
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
<style lang="css">
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
    .banner .social-bottom {
        margin: 0 30px;
    }
    .banner .social-bottom p{
        color: #fff;
        margin: 25px 0 15px;
        font-size: 16px;
        line-height: 18px;
        font-weight: 700;
    }
    .banner .social-bottom a {
        color: #ffffff;
        background: #f3615a;
        width: 70px;
        height: 70px;
        line-height: 70px;
        border-radius: 500px;
        font-size: 30px;
        display: block;
        transition: all 0.3s linear;
    }
    .banner .social-bottom a:hover{
        transform: scale(1.2);
    }
</style>