<template>
    <section class="intro-sec p-0">
        <div id="slider-2-slide-3-layer-1" class="tp-shape tp-shapewrapper rs-layer" data-type="shape" data-rsp_ch="on" data-xy="x:c;y:m;" data-text="fw:100;a:inherit;" data-dim="w:100%;h:100%;" data-basealign="slide" data-frame_1="o:0.8;sR:10;" data-frame_999="o:0;st:w;sR:8690;" style="z-index: 9; background: rgba(0, 0, 0, 0) linear-gradient(rgb(26, 0, 33) 0%, rgb(26, 0, 33) 5%, rgb(38, 6, 51) 40%, rgb(147, 47, 69) 76%, rgb(236, 97, 93) 94%, rgb(236, 97, 93) 100%) repeat scroll 0% 0%; color: rgb(255, 255, 255); position: absolute; display: block; height: 100%; width: 100%; min-width: 0px; max-height: none; max-width: none; transform-origin: 50% 50% 0px; opacity: 0.8; visibility: visible;" data-idcheck="true" data-stylerecorder="true" data-initialised="true">
        </div>
        <div style="z-index: 10;position: absolute; display: block; overflow: visible;color: rgb(255, 255, 255);width:100%;height: 80vh;min-height: 0px;min-width: 0px;max-height: none;max-width: none;transform-origin: 50% 50% 0px;opacity: 0.15;transform: translate(0px);visibility: visible;">
            <img style="" class="img-fluid" src="//the7.io/agency/wp-content/uploads/sites/43/2017/10/art-poly-slider.png" alt="">
        </div>
        <!-- <div id="slider-2-slide-3-layer-12" class="rs-pxl-3 rs-layer" data-type="image" data-rsp_ch="on" data-xy="xo:-663px,-790px,-790px,-663px;yo:-194px;" data-text="l:22;a:inherit;" data-dim="w:['1682px','1682px','1682px','1682px'];h:['750px','750px','750px','750px'];" data-vbility="t,t,f,f" data-basealign="slide" data-frame_0="rY:180;rZ:-43;" data-frame_1="o:0.8;rY:180;rZ:-43;st:400;sp:1000;sR:400;" data-frame_999="o:0;st:w;sR:7600;" style="z-index: 11;
        position: absolute;
        display: block;
        overflow: visible;
        color: rgb(255, 255, 255);
        width: 70vw;
        height: 70vh;
        min-height: 0px;
        min-width: 0px;
        max-height: none;
        max-width: none;
        transform-origin: 50% 50% 0px;
        opacity: 0.8;
        transform: perspective(600px) rotate(-43deg) rotateY(180deg);
        visibility: visible;
        left: -12vw;
        top: -10vh;" data-idcheck="true" data-stylerecorder="true" data-initialised="true">
            <img src="//the7.io/agency/wp-content/uploads/sites/43/2017/10/art-poly-slider.png" alt="" class="tp-rs-img rs-lazyload" data-lazyload="//the7.io/agency/wp-content/uploads/sites/43/2017/10/art-poly-slider.png" data-no-retina="" data-src-rs-ref="//the7.io/agency/wp-content/uploads/sites/43/2017/10/art-poly-slider.png" style="position: relative; height: 100%; width: 100%;" width="2566" height="1144">
        </div>
        
        <div id="slider-2-slide-3-layer-12" class="rs-pxl-3 rs-layer" data-type="image" data-rsp_ch="on" data-xy="xo:-663px,-790px,-790px,-663px;yo:-194px;" data-text="l:22;a:inherit;" data-dim="w:['1682px','1682px','1682px','1682px'];h:['750px','750px','750px','750px'];" data-vbility="t,t,f,f" data-basealign="slide" data-frame_0="rY:180;rZ:-43;" data-frame_1="o:0.8;rY:180;rZ:-43;st:400;sp:1000;sR:400;" data-frame_999="o:0;st:w;sR:7600;" style="z-index: 11;
        position: absolute;
        display: block;
        overflow: visible;
        color: rgb(255, 255, 255);
        width: 70vw;
        height: 70vh;
        min-height: 0px;
        min-width: 0px;
        max-height: none;
        max-width: none;
        transform-origin: 50% 50% 0px;
        opacity: 0.8;
        transform: perspective(600px) rotate(43deg) rotateY(180deg);
        visibility: visible;
        right: -12vw;
        top: -10vh;" data-idcheck="true" data-stylerecorder="true" data-initialised="true">
            <img src="//the7.io/agency/wp-content/uploads/sites/43/2017/10/art-poly-slider.png" alt="" class="tp-rs-img rs-lazyload" data-lazyload="//the7.io/agency/wp-content/uploads/sites/43/2017/10/art-poly-slider.png" data-no-retina="" data-src-rs-ref="//the7.io/agency/wp-content/uploads/sites/43/2017/10/art-poly-slider.png" style="position: relative; height: 100%; width: 100%;" width="2566" height="1144">
        </div> -->
        <div class="intro">
            <div class="row m-0 align-items-center justify-content-center">
                <div class="col-auto text-center">
                    <img src="/assets/images/logo.png" alt="logoImage" style="width: 250px" class="">
                    <h1>OUR <span>SPECIALISTS</span></h1>
                    <img class="scrolldown" src="//the7.io/agency/wp-content/uploads/sites/43/2021/09/arrow-down-40.png" alt="">
                </div>
                
            </div>
        </div>
        <header :class="!topOfPage ? 'onScroll' : '' ">
            <b-navbar  toggleable="lg">
                <b-navbar-brand href="#">
                    <img src="/assets/images/logo.png" alt="logoImage" style="width: 250px" class="navLogo">
                </b-navbar-brand>

                
                <b-collapse id="navbar-toggle-collapse" class="ml-auto justify-content-center" is-nav>
                    <b-navbar-nav class="align-items-center">
                        <b-nav-item active-class="active" :to="localePath('/')" exact>Home</b-nav-item>
                        <b-nav-item :to="localePath('/services')">Services</b-nav-item>
                        <b-nav-item :to="localePath('/faq')">Why Us</b-nav-item>
                        <b-nav-item :to="localePath('/contact')">Case Studies</b-nav-item>
                        <b-nav-item :to="localePath('/about')">About</b-nav-item>
                        <b-nav-item :to="localePath('/blogs')">Blogs</b-nav-item>
                    </b-navbar-nav>
                </b-collapse>
                <div href="#" class="social-header">
                    <a href="#">
                        <font-awesome-icon icon="fa-brands fa-facebook-f" />
                    </a>
                    <a href="#">
                        <font-awesome-icon icon="fa-brands fa-twitter" />
                    </a>
                    <a href="#">
                        <font-awesome-icon icon="fa-solid fa-globe" />
                    </a>
                </div>
                <div>
                    <lang-switch></lang-switch>
                </div>
                <b-navbar-toggle target="navbar-toggle-collapse">
                    <template #default="{ expanded }">
                        <span class="menu-trigger" :class="expanded ? 'active' : ''" id="menu03">
                            <span></span>
                            <span></span>
                            <span></span>
                        </span>
                    </template>
                </b-navbar-toggle>
            </b-navbar>
        </header>
    </section>
</template>

<script>
import langSwitch from '../langSwitch/langSwitch.vue'
import "animate.css/animate.min.css";
export default {
    name: 'AppBlogsHeading',
    data() {
        return {
            show: false,
            show1: false,
            topOfPage: true
        }
    },
    components: {
        langSwitch
    },
    beforeMount() {
        window.addEventListener('scroll', this.handleScroll)
    },
    mounted() {
    },
    methods: {
        handleScroll(){
            let box = document.querySelector('.intro-sec');
            let height = box.offsetHeight;
            if(window.pageYOffset>height){
                if(this.topOfPage) this.topOfPage = false
            } else {
                if(!this.topOfPage) this.topOfPage = true
            }
        },
    }
}
</script>

<style>
    @keyframes sdb07 {
  0% {
    transform: translateY(0);
  }
  50% {
    transform: translateY(10px);
  }
  100% {
    transform: translateY(0);
  }
}
.scrolldown {
  -webkit-animation-delay: 0s;
  animation-delay: 0s;
  animation: sdb07 2s infinite;
}
    .intro-sec {
        background-color: rgba(255, 255, 255, 0);
        background-image: linear-gradient(rgba(0, 0, 0, 0.24) 100%, rgb(255, 255, 255) 100%), url("https://the7.io/agency/wp-content/uploads/sites/43/2017/10/slider-img-01.jpg");
        background-position: center center;
        background-repeat: no-repeat;
        background-size: cover;
        position: relative;
        min-height: 100vh;
    }
    .intro {
        padding: 80px 32px 0;
        z-index: 10;
        position: relative;
        height: calc(100vh - 70px );
        min-height: 600px;
    }
    .intro h1 {
        margin-top: 30px;
        font-size: 100px;
        font-weight: 900;
        letter-spacing: normal;
        line-height: 110px;
        color: #fff;
    }
    .intro h1 span {
        color: rgb(243, 97, 90);
    }
    .intro p {
        color: rgb(243, 97, 90);
        display: block;
        margin-top: 30px;
        font-size: 30px;
        font-style: italic;
        font-weight: 900;
    }
    .intro .btn svg {
        margin-left: 12px;
    }
    .intro .btn:hover {
        color: #fff;
        background-color: transparent;
        border-color: #fff;
    }
    .intro .form {
        width: 438px;
        max-width: 100%;
        padding: 24px;
        border-radius: 12px;
        box-shadow: rgba(0, 0, 0, 0.1) 0px 24px 32px -6px;
        background: #fff;
        margin-bottom: -50px;
    }
    .intro .form img {
        height: 80px;
        width: 80px;
        border-radius: 50%;
    }
    .intro .form h2 {
        font-size: 26px;
        font-weight: 500;
        letter-spacing: -0.416px;
        line-height: 36.4px;
        margin: 12px 0 4px;
    }
    .intro .form h3 {
        font-size: 19px;
        font-weight: 400;
        line-height: 26.4px;
        margin: 12px 0 4px;
        color: rgb(119, 119, 119);
    }
    .intro .form .phone {
        text-decoration: none;
        color: rgb(248, 96, 17);
        font-size: 18px;
        font-weight: 500;
        letter-spacing: -0.18px;
        line-height: 21px;
        margin: 0 0 10px;
        padding: 17px 40px;
        display: inline-block;
    }
    .intro .form svg {
        margin-right: 12px;
    }
    .intro .form input {
        margin: 8px 0;
        padding: 0 18px;
        color: rgb(94, 94, 94);
        font-size: 18px;
        font-weight: 400;
        height: 60px;
        border-radius: 10px;
        border: 1px solid rgb(219, 219, 219);
        color: rgb(94, 94, 94);
    }
    .intro .form input::placeholder {
        color: #a7a7a7;
    }
    .intro .form input:focus {
        border: 1px solid rgb(248, 96, 17);
        box-shadow: none;
    }
    .intro .form .btn {
        padding: 17px 40px;
        background-color: rgb(248, 96, 17);
        display: block;
        margin: 8px 0;
        font-size: 18px;
        font-weight: 500;
        letter-spacing: -0.18px;
        line-height: 21px;
        text-transform: capitalize;
        border-radius: 10px;
        border: 1px solid rgb(248, 96, 17);
        color: #fff;
    }
    .intro .form .btn:hover {
        background-color: rgb(153, 63, 15);
        border: 1px solid rgb(153, 63, 15);
    }
    .intro .form small {
        color: rgb(119, 119, 119);
        font-size: 13px;
        font-weight: 400;
        line-height: 24px;
    }
    header {
        height: 70px;
        padding: 0 20px;
        transition: all 0.1s ease 0s;
        background-color: rgba(0, 0, 0, 0.3);
        z-index: 10;
        position: relative;
    }
    header .navbar {
        padding: 0;
    }
    .navbar-brand {
        padding: 0 50px 0 0;
    }
    .navbar-brand img {
        max-width: 230px;
    }
    .nav-item {
        position: relative;
        margin: 0 12px;
    }
    .nav-item::after {
        content: " ";
        position: absolute;
        left: 18px;
        right: 18px;
        bottom: -24px;
        height: 2px;
        transition: all calc(300 * 1ms) cubic-bezier(.42, .01, .58, 1);
        z-index: 999999998;
        background-color: transparent;
    }
    .nav-item.active::after,
    .nav-item:hover:after {
        background-color: rgb(243, 97, 90);
        left: 18px;
        right: 18px;
        bottom: 18px;
    }
    .nav-link {
        margin: 18px 14px;
        padding: 4px !important;
        font-size: 18px !important;
        font-stretch: 100%;
        font-weight: 700 !important;
        line-height: 22px;
        color: #fff !important;
    }
    .social-header a{
        color: rgb(243, 97, 90);
        display: inline-flex;
        font-size: 16px;
        height: 28px;
        justify-content: center;
        line-height: 28px;
        margin-right: 2px;
        position: relative;
        text-align: center;
        text-decoration-color: rgb(243, 97, 90);
        text-decoration-line: none;
        width: 28px;
        border: 2px solid rgb(243, 97, 90);
        border-radius: 100px;
        align-items: center;
        transition: all .15s linear;
    }
    .social-header a:hover {
        background-color: rgb(243, 97, 90);
        color: #fff;
    }
    .navbar-toggler,
    .navbar-toggler:focus {
        border: none;
        box-shadow: none;
    }
    .menu-trigger,
    .menu-trigger span {
    display: inline-block;
    transition: all .4s;
    box-sizing: border-box;
    }
    .menu-trigger {
    position: relative;
    width: 20px;
    height: 16px;
    background: none;
    border: none;
    appearance: none;
    cursor: pointer;
    }
    .menu-trigger span {
    position: absolute;
    left: 0;
    width: 100%;
    height: 3px;
    background-color:#000;
    border-radius: 4px;
    }
    .menu-trigger span:nth-of-type(1) {
    top: 0;
    }
    .menu-trigger span:nth-of-type(2) {
    top: 6px;
    }
    .menu-trigger span:nth-of-type(3) {
    bottom: 0;
    }
    #menu03.active {
        transform: rotate(360deg);
        }
        #menu03.active span:nth-of-type(1) {
        transform: translateY(6px) rotate(-45deg);
        }
        #menu03.active span:nth-of-type(2) {
        transform: translateY(0) rotate(45deg);
        }
        #menu03.active span:nth-of-type(3) {
        opacity: 0;
        }
    .onScroll {
        position: fixed !important;
        width: 100%;
        display: flex;
        align-items: center;
        transition: all .2s ease-in-out;
        box-shadow: none;
        background-color: rgba(0, 0, 0, 0.8);
        top: 0;
        z-index: 10;
        left: 0;
    }
    .onScroll nav {
        width: 100%;
    }
    @media screen and (max-width: 1049px) {
        header .phone {
            display: none;
        }
    }

    @media screen and (max-width: 991px) {
        nav {
            position: relative;
        }
        .navbar-collapse {
            position: absolute;
            top: 0;
            left: 0;
            right: 0;
        }
        .navbar-collapse.show .navbar-nav {
            position: absolute;
            width: 100%;
            top: 104px;
        }
        .nav-item {
            width: 100%;
            background: #fff;
            text-align: center;
        }
        
        .nav-item:after {
            content: none;
        }
        .nav-item.active .nav-link ,
        .nav-item:hover .nav-link {
            color: rgb(248, 96, 17);
        }
        .nav-link {
            padding: 16px 20px !important;
            font-weight: 500;
            font-size: 18px;
            text-align: center;
        }
    }
</style>