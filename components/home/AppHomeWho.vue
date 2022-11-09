<template>
    <section class="who">
        <div class="row m-0 justify-content-center">
            <h1 class="text-center">THE7 AGENCY. WHO WE ARE</h1>
            <div class="heading-spacer">
                <font-awesome-icon icon="fa-solid fa-angle-down" />
            </div>
        </div>
        <div class="row text">
            <div class="col-lg-6">
                <h2>We are Seven Digital Agency</h2>
                <p>
                    Duis eu libero in lacus venenatis aliquet. Vivamus sagittis tortor et nisi viverra, vel laoreet nisl auctor. Lorem ipsum dolor sit amet, consectetur adipiscing elit.
                </p>
                <p>
                    Fusce iaculis odio nec urna metus vestibulum – commodo egestas, feugiat leo eget vulputate.
                </p>
                <p>
                    Sed elementum, nulla eu varius fermentum, nibh tortor condimentum lacus, at volutpat neque mauris et leo. Donec at neque egestas, feugiat leo eget, ultrices orci. Pellentesque at dui quam. Nullam lorem ipsum – urna metus, vestibulum ac gravida id, aliquet at nunc.
                </p>
                <a href="#" class="btn">View portfolio</a>
                <a href="#" class="btn">Read testimonials</a>
            </div>
            <div class="col-lg-6">
                <div class="image">
                    <img class="img-fluid" src="https://the7.io/agency/wp-content/uploads/sites/43/2017/10/por033-1000x600.jpg" alt="">
                    <div class="overlay">
                    </div>
                </div>
                <p class="after-img">Nunc ac hendrerit <a href="#">Seven Media Presentation</a>  right now.</p>
            </div>
        </div>
        <div class="row who-carousel">

            <swiper :options="swiperOption" class="owl-carousel">
                <swiper-slide>
                <div class="item">
                    <div class="row m-0">
                        <div class="col-auto icon">
                            <font-awesome-icon icon="fa-solid fa-trophy" />
                        </div>
                        <div class="col text">
                            <h3>Premium Quality</h3>
                            <p>
                                Gravida rutrum sit amet – from pellentesque vestibulum nibh diam, nec rhoncus dolor fringilla non. Maecenas ut libero sapien amet.
                            </p>
                        </div>
                    </div>
                </div>
                </swiper-slide>

                <swiper-slide>
                <div class="item">
                    <div class="row m-0">
                        <div class="col-auto icon">
                            <font-awesome-icon icon="fa-solid fa-rocket" />
                        </div>
                        <div class="col text">
                            <h3>Innovative Solutions</h3>
                            <p>
                                Lorem gravida rutrum sit amet id turpis. Pellentesque vestibulum nibh diam, nec rhoncus dolor fringilla non!
                            </p>
                        </div>
                    </div>
                </div>
                </swiper-slide>

                <swiper-slide>
                <div class="item">
                    <div class="row m-0">
                        <div class="col-auto icon">
                            <font-awesome-icon icon="fa-solid fa-comments" />
                        </div>
                        <div class="col text">
                            <h3>Free Consultations</h3>
                            <p>
                                Pellentesque sagittis – sed ac commodo metus. Proin finibus vulputate felis quis iaculis. Hurry up!
                            </p>
                        </div>
                    </div>
                </div>
                </swiper-slide>

                <swiper-slide>
                <div class="item">
                    <div class="row m-0">
                        <div class="col-auto icon">
                            <font-awesome-icon icon="fa-solid fa-sitemap" />
                        </div>
                        <div class="col text">
                            <h3>Multiple Strategies</h3>
                            <p>
                                Gravida rutrum sit amet id turpis. Pellentesque vestibulum nibh diam, nec rhoncus dolor fringilla non. Maecenas ut libero sapien.
                            </p>
                        </div>
                    </div>
                </div>
                </swiper-slide>

                <swiper-slide>
                <div class="item">
                    <div class="row m-0">
                        <div class="col-auto icon">
                            <font-awesome-icon icon="fa-solid fa-users" />
                        </div>
                        <div class="col text">
                            <h3>Experienced Team</h3>
                            <p>
                                Duis eleifend nisl in libero pellentesque sagittis. Sed ac commodo metus. Proin finibus vulputate felis quis iaculis.
                            </p>
                        </div>
                    </div>
                </div>
                </swiper-slide>
            </swiper>

        </div>
    </section>
</template>

<script>
export default {
    name: 'AppHomeWho',
    data() {
        return {
        swiperOption: {
            loop: true,
            slidesPerView: 3,
            spaceBetween: 50,
            breakpoints: {
            // when window width is >= 320px
            100: {
                slidesPerView: 1,
                spaceBetween: 5,
            },
            // when window width is >= 480px
            480: {
                slidesPerView: 1,
                spaceBetween: 5,
            },
            // when window width is >= 640px
            640: {
                slidesPerView: 2,
                spaceBetween: 5,
            },
            992: {
                slidesPerView: 2,
                spaceBetween: 5,
            },
            1200: {
                slidesPerView: 3,
                spaceBetween: 5,
            },
            },
        },
           
        }
    },
    
    methods: {
        
    }
}
</script>
<style lang="css">
 .who {
     padding: 80px 50px 100px;
 }
 .who h1 {
     color: rgb(51, 51, 51);
    font-size: 42px;
    font-weight: 700;
    line-height: 52px;
 }
 .who .heading-spacer {
    margin-bottom: 60px;
    height: 21px;
    position: relative;
    overflow: hidden;
    text-align: center;
 }
 .who .heading-spacer svg {
    color: var(--main-color);
    font-size: 26px;
 }
 .who .heading-spacer::before {
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
 .who .heading-spacer::after {
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
 .who .text h2{
    color: rgb(51, 51, 51);
    font-size: 26px;
    font-weight: 700;
    line-height: 36px;
    margin-bottom: 20px
 }
 .who .text p{
    color: rgb(133, 134, 140);
    font-size: 16px;
    font-weight: 400;
    line-height: 26px;
    margin-bottom: 10px
 }
 .who .text .btn{
    color: rgb(255, 255, 255);
    font-size: 13px;
    margin-bottom: 10px;
    margin-right: 10px;
    padding-bottom: 7px;
    padding-left: 14px;
    padding-right: 14px;
    padding-top: 8px;
    text-align: center;
    background-color: #f3615a;
    border-radius: 0;
    width: 180px;
    font-weight: 700;
    text-transform: uppercase;
 }
 .who .image {
     position: relative;
     padding-left: 25px;
 }
 .who .image .overlay {
    position: absolute;
    left: 25px;
    right: 0;
    top: 0;
    height: 100%;
    z-index: 1;
    opacity: 0;
    background: linear-gradient(135deg,rgba(38, 6, 51, 0.25) 30%,rgba(236,97,93,0.8) 100%);
    transition: all 0.3s linear;;
 }
 .who .image:hover .overlay {
     opacity: 1;
 }
 .who .after-img {
    margin-top: 10px;
    text-align: center;
    color: rgb(180, 181, 187);
    font-size: 16px;
 }
 .who a ,
 .who a:hover {
     color: var(--main-color)
 }

 .who .item .icon {
    background: rgba(255,255,255,0.01);
    border: 3px solid var(--main-color);
    width: 60px;
    height: 60px;
    line-height: 60px;
    border-radius: 0px;
    font-size: 24px;
    display: inline-block;
    color: var(--main-color);
    text-align: center;
 }
 .who .item .text h3 {
    color: rgb(51, 51, 51);
    font-size: 20px;
    line-height: 30px;
    margin: 0;
 }
 .who .item .text p {
    color: rgb(133, 134, 140);
    float: left;
    font-size: 16px;
    margin-top: 10px;
    margin-bottom: 0;
 }
</style>