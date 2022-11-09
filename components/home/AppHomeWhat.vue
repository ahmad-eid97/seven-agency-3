<template>
    <section class="what">
        <div class="row m-0">
            <div class="col-lg-6 image">
            </div>
            <div class="col-lg-6 text" style="padding: 80px 0 60px">
                <div class="row m-0 ">
                    <h1 class="text-center">WHAT CLIENTS SAY</h1>
                    <div class="heading-spacer">
                        <font-awesome-icon icon="fa-solid fa-angle-down" />
                    </div>
                </div>
                <div class="row what-carousel">

                    <swiper :options="swiperOption" class="owl-carousel">
                        <swiper-slide>
                        <div class="item">
                            <div class="row m-0 justify-content-center">
                                <div class="col-auto user">
                                    <img src="https://the7.io/agency/wp-content/uploads/sites/43/2017/10/t002-90x90.jpg" alt="">
                                </div>
                                <div class="col-12 text">
                                    <h3>Richard Brown</h3>
                                    <h4>
                                        Business owner - Seven commerce
                                    </h4>
                                    <p>
                                        I want to say lorem ipsum dolor amet! Proin nisl risus, tincidunt sed rutrum nec, imperdiet ac enim. Morbi faucibusd ac – lorem glavrida liquam lorem ipsum dolor erat volutpat.
                                    </p>
                                </div>
                            </div>
                        </div>
                        </swiper-slide>

                        <swiper-slide>
                        <div class="item">
                            <div class="row m-0 justify-content-center">
                                <div class="col-auto user">
                                    <img src="https://the7.io/agency/wp-content/uploads/sites/43/2017/10/t003-90x90.jpg" alt="">
                                </div>
                                <div class="col-12 text">
                                    <h3>Anna Wildfire</h3>
                                    <h4>
                                        Creative director - Seven digital
                                    </h4>
                                    <p>
                                        Gravida rutrum sit amet dolor from pellentesque vestibulum nibh diam, nec rhoncus dolor fringilla lorem ipsim dolor non! Vestibulum nibh diam, nec rhoncus dolor. Thanx!
                                    </p>
                                </div>
                            </div>
                        </div>
                        </swiper-slide>

                        <swiper-slide>
                        <div class="item">
                            <div class="row m-0 justify-content-center">
                                <div class="col-auto user">
                                    <img src="https://the7.io/agency/wp-content/uploads/sites/43/2017/10/t001-90x90.jpg" alt="">
                                </div>
                                <div class="col-12 text">
                                    <h3>Alexander Smith</h3>
                                    <h4>
                                        Marketing director - Seven arts
                                    </h4>
                                    <p>
                                        I want to say lorem ipsum dolor amet! Proin nisl risus, tincidunt sed rutrum nec, imperdiet ac enim. Morbi faucibusd ac – lorem glavrida liquam lorem ipsum dolor erat volutpat.
                                    </p>
                                </div>
                            </div>
                        </div>
                        </swiper-slide>
                    </swiper>

                </div>
                <div class="row brands justify-content-between">
                    <div class="brand">
                        <img class="img-fluid" src="https://the7.io/agency/wp-content/uploads/sites/43/2017/10/4-logo-18-400x300.png" alt="">
                    </div>
                    <div class="brand">
                        <img class="img-fluid" src="https://the7.io/agency/wp-content/uploads/sites/43/2017/10/4-logo-09-400x300.png" alt="">
                    </div>
                    <div class="brand">
                        <img class="img-fluid" src="https://the7.io/agency/wp-content/uploads/sites/43/2017/10/4-logo-12-400x300.png" alt="">
                    </div>
                    <div class="brand">
                        <img class="img-fluid" src="https://the7.io/agency/wp-content/uploads/sites/43/2017/10/4-logo-23-400x300.png" alt="">
                    </div>
                    <div class="brand">
                        <img class="img-fluid" src="https://the7.io/agency/wp-content/uploads/sites/43/2017/10/4-logo-19-400x300.png" alt="">
                    </div>
                    <div class="brand">
                        <img class="img-fluid" src="https://the7.io/agency/wp-content/uploads/sites/43/2017/10/4-logo-14-400x300.png" alt="">
                    </div>
                </div>
            </div>
        </div>
    </section>
</template>

<script>
export default {
    name: 'AppHomeWhat',
    data() {
        return {
            swiperOption: {
                loop: true,
                slidesPerView: 1,
                spaceBetween: 50,
            }
           
        }
    },
    
    methods: {
        
    }
}
</script>
<style lang="css">
 .what {
     padding: 0;
 }
 .what h1 {
    color: rgb(51, 51, 51);
    font-size: 42px;
    font-weight: 700;
    line-height: 52px;
 }
 .what .heading-spacer {
    margin-bottom: 60px;
    height: 21px;
    position: relative;
    overflow: hidden;
    text-align: center;
 }
 .what .heading-spacer svg {
    color: var(--main-color);
    font-size: 26px;
 }
 .what .heading-spacer::before {
    content: "";
    position: absolute;
    bottom: 50%;
    right: 0;
    top: 40%;
    width: 60px;
    border-style: solid;
    border-color: #f3615a;
    border-bottom-width: 1px;
    left: 36%;
 }
 .what .heading-spacer::after {
    content: "";
    position: absolute;
    bottom: 50%;
    right: 0;
    top: 40%;
    width: 60px;
    border-style: solid;
    border-color: #f3615a;
    border-bottom-width: 1px;
    right: 36%;
 }
 .what .item {
    padding: 70px;
 }
 .what .item .text{
    text-align: center;
 }
 .what .item .text h3{
    font-size: 20px;
    font-weight: 700;
    letter-spacing: normal;
    line-height: 30px;
    color: rgb(51, 51, 51)
 }
 .what .item .text h4{
    color: var(--main-color);
    font-size: 16px;
    font-weight: 700;
    letter-spacing: normal;
    line-height: 28px;
 }
 .what .item .text p{
    color: rgb(133, 134, 140);
    font-size: 20px;
    font-style: italic;
    letter-spacing: normal;
    line-height: 32px;
 }
 
 .what .image {
    padding-top: 150px !important;
    padding-bottom: 150px !important;
    background-image: url(https://the7.io/agency/wp-content/uploads/sites/43/2017/10/bg001.jpg?id=631) !important;
    background-position: center !important;
    background-repeat: no-repeat !important;
    background-size: cover !important;

 }
 
 .what .item .user {
    width: 90px;
    height: 90px;
    border-radius: 50%;
    padding: 0;
    overflow: hidden;
    margin-bottom: 15px;
 }
 .what .item .item-text h3 {
    color: rgb(51, 51, 51);
    font-size: 20px;
    line-height: 30px;
    margin: 0;
 }
 .what .item .item-text p {
    color: rgb(133, 134, 140);
    float: left;
    font-size: 16px;
    margin-top: 10px;
    margin-bottom: 0;
 }
 .what .brands {
     padding: 0 20px;
 }
 .what .brands .brand {
     width: 90px;
     height: 67.5px;
     padding: 0;
 }
</style>