<template>
    <section class="owner">
        <div class="row m-0">
            <div class="col-lg-6 text">
                <div class="row m-0 justify-content-center">
                    <div class="col-auto user">
                        <img class="img-fluid" src="https://the7.io/agency/wp-content/uploads/sites/43/2017/10/t002-440x440.jpg" alt="">
                    </div>
                    <div class="col-12 text">
                        <h2>RICHARD SMITH</h2>
                        <h4>
                            Economist. Agency owner.
                        </h4>
                        <p>
                            Vestibulum posuere felis vestibulum pharetra dapibus. Nam vitae sapien dapibus, condimentum ipsum non, porttitor purus. Cras et diam ac – nunc urna magna, porttitor eu laoreet aliquam, pellentesque eu velit. Suspendisse potenti!
                        </p>
                        <span class="contact">
                            <font-awesome-icon icon="fa-solid fa-phone-flip" />
                            001 234 56 78
                        </span>
                        <span class="contact">
                            <font-awesome-icon icon="fa-solid fa-envelope" />
                            richard@dream-theme.com
                        </span>
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
            <div class="col-lg-6 image">

            </div>
            
        </div>
    </section>
</template>

<script>
export default {
    name: 'AppHomeOwner',
    data() {
        return {
           
        }
    },
    
    methods: {
        
    }
}
</script>
<style lang="scss">
 .owner {
     padding: 0;
 }
 
 .owner .user{
    margin: 80px 0 30px;
    padding: 0;
    width: 220px;
    height: 220px;
    border-radius: 50%;
    overflow: hidden;
 }
 .owner .text {
     background-color: #f7f7f7;
     padding-bottom: 60px
 }
 .owner .text h2{
    color: rgb(51, 51, 51);
    font-size: 42px;
    font-weight: 700;
    line-height: 52px;
    text-align: center;
 }
 .owner .text h4{
    color: var(--main-color);
    font-size: 24px;
    font-weight: 700;
    line-height: 34px;
    margin-bottom: 25px;
    text-align: center;
 }
 .owner .text p{
    color: rgb(133, 134, 140);
    font-size: 16px;
    text-align: center;
    padding: 0 90px;
    line-height: 30px;
    margin: 0;
    padding-bottom: 25px;
 }
 @include xs {
    .owner .text p{
        font-size: 16px;
        padding: 0 20px;
        line-height: 30px;
    }
 }
 .owner .text .contact{
    color: var(--main-color);
    display: block;
    font-size: 16px;
    font-weight: 700;
    line-height: 28px;
    margin-bottom: 10px;
    text-align: center;
 }
 .social-owner {
     display: flex;
     justify-content: center;
 }
.social-owner a{
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
    border: 2px solid var(--main-color);
    border-radius: 100px;
    align-items: center;
    transition: all .15s linear;
    
}
.social-owner a:hover {
    background-color: var(--main-color);
    color: #fff;
}
 .owner .image {
    padding-top: 150px !important;
    padding-bottom: 150px !important;
    background-image: url(https://the7.io/agency/wp-content/uploads/sites/43/2017/10/bg006.jpg?id=733) !important;
    background-position: center !important;
    background-repeat: no-repeat !important;
    background-size: cover !important;

 }
 
 .owner .item .icon {
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
 .owner .item .item-text h3 {
    color: rgb(51, 51, 51);
    font-size: 20px;
    line-height: 30px;
    margin: 0;
 }
 .owner .item .item-text p {
    color: rgb(133, 134, 140);
    float: left;
    font-size: 16px;
    margin-top: 10px;
    margin-bottom: 0;
 }
</style>