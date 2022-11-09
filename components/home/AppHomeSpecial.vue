<template>
    <section class="special">
        <div class="row m-0 justify-content-center">
            <h1 class="text-center">OUR SPECIALISTS</h1>
            <div class="heading-spacer">
                <font-awesome-icon icon="fa-solid fa-angle-down" />
            </div>
        </div>
        <div class="row special-carousel">

            <swiper :options="swiperOption" class="owl-carousel">

                <swiper-slide>
                <div class="item">
                    <div class="row m-0 justify-content-center">
                        <div class="col-auto user">
                            <img src="https://the7.io/agency/wp-content/uploads/sites/43/2017/10/t007.jpg" alt="">
                        </div>
                        <div class="col-12 text">
                            <h3>Logan White</h3>
                            <h4>
                                Photographer
                            </h4>
                            <p>
                                Nullam volutpat mauris eu erat accumsan, sit amet lobortis odio finibus. Phasellus tempor leo sed est pretium, a malesuada quam lacinia.
                            </p>
                            <div href="#" class="social-owner">
                                <a href="#">
                                    <font-awesome-icon icon="fa-brands fa-behance" />
                                </a>
                                <a href="#">
                                    <font-awesome-icon icon="fa-brands fa-instagram" />
                                </a>
                                <a href="#">
                                    <font-awesome-icon icon="fa-brands fa-facebook-f" />
                                </a>
                                <a href="#">
                                    <font-awesome-icon icon="fa-brands fa-twitter" />
                                </a>
                            </div>
                        </div>
                    </div>
                </div>
                </swiper-slide>

                <swiper-slide>
                <div class="item">
                    <div class="row m-0 justify-content-center">
                        <div class="col-auto user">
                            <img src="https://the7.io/agency/wp-content/uploads/sites/43/2017/10/t004.jpg" alt="">
                        </div>
                        <div class="col-12 text">
                            <h3>Lucas Brown</h3>
                            <h4>
                                Programmer
                            </h4>
                            <p>
                                Maecenas lorem ipsum dolor eget erat molestie, tincidunt est cursus, dapibus nulla. Nullam quis enim eu odio pretium aliquet. 
                            </p>
                            <div href="#" class="social-owner">
                                <a href="#">
                                    <font-awesome-icon icon="fa-brands fa-behance" />
                                </a>
                                <a href="#">
                                    <font-awesome-icon icon="fa-brands fa-instagram" />
                                </a>
                                <a href="#">
                                    <font-awesome-icon icon="fa-brands fa-facebook-f" />
                                </a>
                                <a href="#">
                                    <font-awesome-icon icon="fa-brands fa-twitter" />
                                </a>
                            </div>
                        </div>
                    </div>
                </div>
                </swiper-slide>

                <swiper-slide>
                <div class="item">
                    <div class="row m-0 justify-content-center">
                        <div class="col-auto user">
                            <img src="https://the7.io/agency/wp-content/uploads/sites/43/2017/10/t003.jpg" alt="">
                        </div>
                        <div class="col-12 text">
                            <h3>Olivia Walsh</h3>
                            <h4>
                                Marketing director
                            </h4>
                            <p>
                                Vestibulum posuere felis vestibulum pharetra dapibus. Nam vitae sapien dapibus, condimentum ipsum non, porttitor purus.
                            </p>
                            <div href="#" class="social-owner">
                                <a href="#">
                                    <font-awesome-icon icon="fa-brands fa-behance" />
                                </a>
                                <a href="#">
                                    <font-awesome-icon icon="fa-brands fa-instagram" />
                                </a>
                                <a href="#">
                                    <font-awesome-icon icon="fa-brands fa-facebook-f" />
                                </a>
                                <a href="#">
                                    <font-awesome-icon icon="fa-brands fa-twitter" />
                                </a>
                            </div>
                        </div>
                    </div>
                </div>
                </swiper-slide>

                <swiper-slide>
                <div class="item">
                    <div class="row m-0 justify-content-center">
                        <div class="col-auto user">
                            <img src="https://the7.io/agency/wp-content/uploads/sites/43/2017/10/t001.jpg" alt="">
                        </div>
                        <div class="col-12 text">
                            <h3>Alex Green</h3>
                            <h4>
                                Account manager
                            </h4>
                            <p>
                                Cras et diam ac – nunc urna magna, porttitor eu laoreet aliquam, pellentesque eu velit. Suspendisse potenti.
                            </p>
                            <div href="#" class="social-owner">
                                <a href="#">
                                    <font-awesome-icon icon="fa-brands fa-behance" />
                                </a>
                                <a href="#">
                                    <font-awesome-icon icon="fa-brands fa-instagram" />
                                </a>
                                <a href="#">
                                    <font-awesome-icon icon="fa-brands fa-facebook-f" />
                                </a>
                                <a href="#">
                                    <font-awesome-icon icon="fa-brands fa-twitter" />
                                </a>
                            </div>
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
    name: 'AppHomeSpecial',
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
 .special {
     padding: 80px 50px 100px;
 }
 .special h1 {
     color: rgb(51, 51, 51);
    font-size: 42px;
    font-weight: 700;
    line-height: 52px;
 }
 .special .heading-spacer {
    margin-bottom: 60px;
    height: 21px;
    position: relative;
    overflow: hidden;
    text-align: center;
 }
 .special .heading-spacer svg {
    color: var(--main-color);
    font-size: 26px;
 }
 .special .heading-spacer::before {
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
 .special .heading-spacer::after {
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
 .special .item {
     padding: 20px 0 30px;
 }
 .special .item .user{
    width: 140px;
    height: 140px;
    border-radius: 50%;
    overflow: hidden;
    padding: 0;
 }
 .special .item .text{
    text-align: center;
 }
 .special .item .text h3{
    font-size: 20px;
    font-weight: 700;
    letter-spacing: normal;
    line-height: 30px;
    color: rgb(51, 51, 51)
 }
 .special .item .text h4{
    color: var(--main-color);
    font-size: 16px;
    font-weight: 700;
    letter-spacing: normal;
    line-height: 28px;
 }
 .special .item .text p{
    color: rgb(133, 134, 140);
    font-size: 16px;
    font-style: italic;
    letter-spacing: normal;
    line-height:  26px;
    margin-bottom: 10px
 }
 .special .social-owner {
     display: flex;
     justify-content: center;
 }
.special .social-owner a{
    color: var(--main-color);
    display: inline-flex;
    font-size: 16px;
    height: 28px;
    justify-content: center;
    line-height: 28px;
    margin-right: 5px;
    position: relative;
    text-align: center;
    text-decoration-color: var(--main-color);
    text-decoration-line: none;
    width: 28px;
    border: 2px solid transparent;
    border-radius: 100px;
    align-items: center;
    transition: all .15s linear;
    
}
.special .social-owner a:hover {
    background-color: var(--main-color);
    color: #fff;
}
</style>