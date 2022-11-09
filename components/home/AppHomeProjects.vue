<template>
    <section class="projects">
       <div class="row m-0 justify-content-center">
            <h1 class="text-center">CHECK OUT OUR PROJECTS!</h1>
            <div class="heading-spacer">
                <font-awesome-icon icon="fa-solid fa-angle-down" />
            </div>
        </div>
        <div class="row">
            <CoolLightBox 
                :items="items" 
                :index="index"
                @close="index = null">
            </CoolLightBox>
            <div class="images-wrapper">
                <div class="row justify-content-between m-0">
                    <div
                        class="col-md-6 col-lg-4 my-3 project"
                        v-for="(image, imageIndex) in items"
                        :key="imageIndex"
                        @click="index = imageIndex"
                    >
                        <div class="image" :style="{ backgroundImage: 'url(' + image + ')' }">
                            <div class="rollover">
                                <div class="rollover-content">
                                    <a class="rollover-link" href="#">
                                        <font-awesome-icon icon="fa-solid fa-arrow-up-right-from-square" />
                                    </a>
                                    <a class="rollover-link" href="#">
                                        <font-awesome-icon icon="fa-solid fa-expand" />
                                    </a>
                                    <a class="rollover-link" href="#">
                                        <font-awesome-icon icon="fa-solid fa-plus" />
                                    </a>
                                </div>
                            </div>
                        </div>
                        <h3>Glavrida lorem pouch</h3>
                        <p class="meta">Products</p>
                        <p>
                            Duis eu libero in lacus venenatis aliquet. Vivamus sagittis tortor et nisi viverra, vel laoreet nisl auctor.
                        </p>
                    </div>
                </div>
            </div>
        </div>
        <div class="row mx-0 mt-5 justify-content-center">
            <div class="col-auto">
                <a href="#" class="btn">VIEW ALL WORK</a>
            </div>
        </div>
    </section>
</template>

<script>
import "animate.css/animate.min.css";
export default {
    name: 'AppHomeProjects',
    data() {
        return {
            items: [
                'https://the7.io/agency/wp-content/uploads/sites/43/2017/10/por006-768x512.jpg',
                'https://the7.io/agency/wp-content/uploads/sites/43/2017/10/por005-768x768.jpg',
                'https://the7.io/agency/wp-content/uploads/sites/43/2017/10/por013-768x512.jpg',
                'https://the7.io/agency/wp-content/uploads/sites/43/2017/10/por012-768x512.jpg',
                'https://the7.io/agency/wp-content/uploads/sites/43/2017/10/por016-768x512.jpg',
                'https://the7.io/agency/wp-content/uploads/sites/43/2017/10/por004-768x768.jpg'
            ],
            index: null
        }
    },
    methods: {
        
    }
}
</script>
<style lang="css">
    .projects {
        padding-top: 80px;
        padding-bottom: 60px;
    }
    .projects h1 {
        color: rgb(51, 51, 51);
        font-size: 42px;
        font-weight: 700;
        line-height: 52px;
    }
    .projects .heading-spacer {
        margin-bottom: 60px;
        height: 21px;
        position: relative;
        overflow: hidden;
        text-align: center;
    }
    .projects .heading-spacer svg {
        color: var(--main-color);
        font-size: 26px;
    }
    .projects .heading-spacer::before {
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
    .projects .heading-spacer::after {
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
    .projects .image {
        height: 295px;
        background-size: cover;
        position: relative;
    }
    
    .projects .image .rollover {
        transform: scaleY(0);
        background: linear-gradient(135deg,rgba(38,6,51,0.8) 30%,rgba(236,97,93,0.8) 100%);
        opacity: 0;
        display: flex;
        display: flex;
        align-items: center;
        justify-content: space-around;
        position: absolute;
        top: 0;
        right: 0;
        bottom: 0;
        left: 0;
        width: 100%;
        height: 100%;
        line-height: normal;
        text-align: center;
        transition: all .3s ease-in-out;
        -webkit-transform-style: preserve-3d;
    }
    .projects .image:hover .rollover {
        transform: scaleY(1);
        opacity: 1;
    }
    .projects .image .rollover-content {
        padding: 10px;
        width: 90%;
        box-sizing: border-box;
        line-height: normal;
        text-align: center;
    }
    
    .projects .image .rollover-content .rollover-link {
        width: 44px;
        height: 44px;
        line-height: 44px;
        border-radius: 100px;
        margin: 10px 5px 10px;
        background-color: rgba(255, 255, 255, 0.3);
        color: #fff;
        padding: 12px 15px;
    }


    .projects .project {
        padding-bottom: 15px;
        padding-left: 25px;
        padding-right: 25px;
        padding-top: 20px
    }

    .projects .project h3 {
        color: rgb(51, 51, 51);
        font-size: 20px;
        font-weight: 700;
        margin-bottom: 5px;
        padding-top: 25px;
        text-align: center;
    }
    .projects .project .meta {
        color: rgb(180, 181, 187);
        font-size: 13px;
        line-height: 23px;
        text-align: center;
        margin-bottom: 16px
    }
    .projects .project p {
        color: rgb(133, 134, 140);
        font-size: 14px;
        line-height: 25px;
        margin-bottom: 10px;
        text-align: center;
    }
    .projects .btn {
        border: 1px solid rgba(51, 51, 51, 0.1);
        border-radius: 0;
       color: rgb(51, 51, 51);
       font-size: 14px;
       padding: 14px 40px;
    }
</style>