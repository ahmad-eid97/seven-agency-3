<template>
    <section class="contact">
        <div class="row m-0">
            <div class="col-lg-6 text">
                <div class="row m-0 ">
                    <h1 class="text-center">CONTACT INFO</h1>
                    <div class="heading-spacer">
                        <font-awesome-icon icon="fa-solid fa-angle-down" />
                    </div>
                </div>
                <div class="row m-0">
                    <div class="items">
                        <div class="item">
                            <div class="row m-0 align-items-center">
                                <div class="col-auto icon">
                                    <font-awesome-icon icon="fa-solid fa-signs-post" />
                                </div>
                                <div class="col item-text">
                                    <h3>
                                        SoHo 94 Broadway St New York, NY 1001
                                    </h3>
                                </div>
                            </div>
                        </div>
                        <div class="item">
                            <div class="row m-0 align-items-center">
                                <div class="col-auto icon">
                                    <font-awesome-icon icon="fa-solid fa-phone" />
                                </div>
                                <div class="col item-text">
                                    <h3>001 234 56 78</h3>
                                </div>
                            </div>
                        </div>
                        <div class="item">
                            <div class="row m-0 align-items-center">
                                <div class="col-auto icon">
                                    <font-awesome-icon icon="fa-solid fa-envelope" />
                                </div>
                                <div class="col item-text">
                                    <h3>hello@dream-theme.com</h3>
                                </div>
                            </div>
                        </div>
                        <div class="item">
                            <div class="row m-0 align-items-center">
                                <div class="col-auto icon">
                                    <font-awesome-icon icon="fa-solid fa-clock" />
                                </div>
                                <div class="col item-text">
                                    <h3>Mon. - Fri. 10:00 - 19:00</h3>
                                </div>
                            </div>
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
    name: 'AppHomecontact',
    data() {
        return {
           
        }
    },
    
    methods: {
        
    }
}
</script>
<style lang="css">
 .contact {
     padding: 0;
 }
 .contact h1 {
     color: rgb(51, 51, 51);
    font-size: 42px;
    font-weight: 700;
    line-height: 52px;
 }
 .contact .heading-spacer {
    margin-bottom: 60px;
    height: 21px;
    position: relative;
    overflow: hidden;
    text-align: center;
 }
 .contact .heading-spacer svg {
    color: var(--main-color);
    font-size: 26px;
 }
 .contact .heading-spacer::before {
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
 .contact .heading-spacer::after {
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
 .contact .text{
    background-color: #f7f7f7;
    padding: 80px 5% 60px;
 }
 .contact .text p{
    color: rgb(133, 134, 140);
    font-size: 16px;
    font-weight: 400;
    line-height: 26px;
    padding-bottom: 35px;
    text-align: center;
 }
 .contact .text .btn{
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
 .contact .image {
    padding-top: 150px !important;
    padding-bottom: 150px !important;
    background-image: url(https://the7.io/agency/wp-content/uploads/sites/43/2017/10/bg009.jpg?id=740) !important;
    background-position: center !important;
    background-repeat: no-repeat !important;
    background-size: cover !important;

 }

 .contact .item  {
     margin-bottom: 30px;
 }
 
 .contact .item .icon {
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
 .contact .item .item-text h3 {
    color: rgb(51, 51, 51);
    font-size: 20px;
    line-height: 30px;
    margin: 0;
 }
 .contact .item .item-text p {
    color: rgb(133, 134, 140);
    float: left;
    font-size: 16px;
    margin-top: 10px;
    margin-bottom: 0;
 }
</style>