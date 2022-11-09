<template>
    <section class="Message">
        <div class="row m-0">
            <div class="col-lg-6 image">
            </div>
            <div class="col-lg-6 text">
                <div class="row m-0 ">
                    <h1 class="text-center">DROP US A LINE</h1>
                    <div class="heading-spacer">
                        <font-awesome-icon icon="fa-solid fa-angle-down" />
                    </div>
                    <p>
                        Aliquam ex sem, iaculis at interdum non, bibendum non est. In mi sapien, consequat ut consequat eget!
                    </p>
                </div>
                <div class="row m-0">
                    <div class="items">
                        <div class="item">
                              <input type="text" class="form-control" id="exampleFormControlInput1" placeholder="Name *">
                        </div>
                        <div class="item">
                            <input type="email" class="form-control" id="exampleFormControlInput1" placeholder="E-mail *">
                        </div>
                        <div class="item">
                            <input type="text" class="form-control" id="exampleFormControlInput1" placeholder="Telephone *">
                        </div>
                        <div class="item">
                            <textarea  placeholder="Messages *" class="form-control" id="exampleFormControlTextarea1" rows="3"></textarea>
                        </div>
                        <a href="#" class="btn mt-3">Send Message</a>
                    </div>
                </div>
            </div>
        </div>
    </section>
</template>

<script>
export default {
    name: 'AppHomeMessage',
    data() {
        return {
           
        }
    },
    
    methods: {
        
    }
}
</script>
<style lang="css">
 .Message {
     padding: 0;
 }
 .Message h1 {
     color: rgb(51, 51, 51);
    font-size: 42px;
    font-weight: 700;
    line-height: 52px;
 }
 .Message .heading-spacer {
    margin-bottom: 60px;
    height: 21px;
    position: relative;
    overflow: hidden;
    text-align: center;
 }
 .Message .heading-spacer svg {
    color: var(--main-color);
    font-size: 26px;
 }
 .Message .heading-spacer::before {
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
 .Message .heading-spacer::after {
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
 .Message .text{
    background-color: #f7f7f7;
    padding: 80px 5% 60px;
 }
 .Message .text p{
    color: rgb(133, 134, 140);
    font-size: 16px;
    font-weight: 400;
    line-height: 26px;
    padding-bottom: 35px;
    text-align: center;
 }
 .Message .text .btn{
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
 .Message .image {
    padding-top: 150px !important;
    padding-bottom: 150px !important;
    background-image: url(https://the7.io/agency/wp-content/uploads/sites/43/2017/10/bg002.jpg?id=632) !important;
    background-position: center !important;
    background-repeat: no-repeat !important;
    background-size: cover !important;

 }

 .Message .item  {
    margin-bottom: 10px;
 }

 .Message .item .form-control {
    border-radius: 0;
 }

 .Message .item .form-control::placeholder {
    color: rgba(139, 141, 148, 0.7);
 }
 
 
</style>