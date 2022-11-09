<template>
    <section class="process">
        <div class="row m-0 justify-content-center content">
            <h2 class="text-center">OUR PROCESS</h2>
            <div class="heading-spacer">
                <font-awesome-icon icon="fa-solid fa-angle-down" />
            </div>
            <div class="icons">
                <ul class="icon_list top">
                    <div class="row justify-content-center">

                        <div class="col-6">
                            
                            <li class="icon_list_item">
                                <div class="icon_list_icon">
                                    <font-awesome-icon icon="fa-solid fa-square-phone" />
                                </div>
                                <h3>1.</h3>
                                <div class="icon_list_connector"></div>
                            </li>

                        </div>

                        <div class="col-6">
                            
                            <li class="icon_list_item">
                                <div class="icon_list_icon">
                                    <font-awesome-icon icon="fa-solid fa-list-ol" />
                                </div>
                                <h3>2.</h3>
                            </li>
                            
                        </div>

                    </div>
                </ul>
            </div>
            <div class="row m-0  justify-content-center">
                <div class="col-lg-6 text">
                    <h3>
                        First Contact
                    </h3>
                    <p>
                        Feugiat leo eget, ultrices orci. Pellentesque at dui quam. Nullam lorem ipsum – urna metus, vestibulum ac gravida id, aliquet at nunc.
                    </p>
                </div>
                <div class="col-lg-6 text">
                    <h3>
                        Discussion & Planning
                    </h3>
                    <p>
                        Duis ac turpis a tellus posuere condimentum vitae vitae libero. Curabitur aliquet vitae nulla nec posuere.
                    </p>
                </div>
            </div>
            <div class="icons">
                <ul class="icon_list top">
                    <div class="row"></div>
                    <li class="icon_list_item">
                        <div class="icon_list_icon">
                            <font-awesome-icon icon="fa-solid fa-suitcase" />
                        </div>
                        <h3>3.</h3>
                        <div class="icon_list_connector"></div>
                    </li>
                    <li class="icon_list_item">
                        <div class="icon_list_icon">
                            <font-awesome-icon icon="fa-solid fa-wand-magic-sparkles" />
                        </div>
                        <h3>4.</h3>
                        <div class="icon_list_connector"></div>
                    </li>
                    <li class="icon_list_item">
                        <div class="icon_list_icon">
                            <font-awesome-icon icon="fa-solid fa-maximize" />
                        </div>
                        <h3>5.</h3>
                    </li>
                </ul>
            </div>
            <div class="row m-0  justify-content-center">
                <div class="col-lg-4 text">
                    <h3>
                        Final Strategy
                    </h3>
                    <p>
                        Quisque facilisis fringilla fringilla. Pellentesque fermentum dignissim viverra. Etiam nec nunc est. In vehicula justo vitae ipsum convallis!
                    </p>
                </div>
                <div class="col-lg-4 text">
                    <h3>
                        Implementation
                    </h3>
                    <p>
                        Proin nisl risus, tincidunt sed rutrum nec, imperdiet ac enim. Morbi faucibusd ac – lorem glavrida liquam erat volutpat.
                    </p>
                </div>
                <div class="col-lg-4 text">
                    <h3>
                        Control
                    </h3>
                    <p>
                        Donec a tincidunt dui. Aenean quis nisi lectus. Ut dignissim, erat non viverra accumsan, magna nunc adipiscing elit. Cras accumsan nisi lacus, id faucibus lorem molestie non.
                    </p>
                </div>
            </div>
            
        </div>
        
    </section>
</template>

<script>
export default {
    name: 'AppHomeProcess',
    data() {
        return {
           
        }
    },
    
    methods: {
        
    }
}
</script>
<style lang="scss">
    .process {
        background-size: cover;
        background-repeat: no-repeat;
        background-color: rgba(0, 0, 0, 0);
        background-image: url("https://the7.io/agency/wp-content/uploads/sites/43/2017/10/bg003.jpg") ;
        background-attachment: scroll;
        padding: 60px 30px 80px;
        position: relative;
    }
    .process::after {
        top: 0;
        bottom: 0;
        left: 0;
        right: 0;
        background-color: rgba(26,0,33,0.9);
        position: absolute;
        content: "";
        z-index: 0;
    }
    .process .content {
        z-index: 1;
        position: relative;
    }
    .process h2 {
        color: #ffffff;
        font-weight: 700;
        font-size: 42px;
        line-height: 52px;
    }
    @include md {
        .icon_list_connector {
            display: none;
        }
    }
    .process .heading-spacer {
        margin-bottom: 60px;
        height: 21px;
        position: relative;
        overflow: hidden;
        text-align: center;
    }
    .process .heading-spacer svg {
        color: var(--main-color);
        font-size: 26px;
    }
    .process .heading-spacer::before {
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
    .process .heading-spacer::after {
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
    .process .icons {
        padding: 25px 25px 0;
    }
    .process ul {
        list-style: none;
        justify-content: center;
        display: flex;
    }
    .process .icon_list_item {
        // width: 385px;
        position: relative;
        display: table-cell;
    }
    .process .icon_list_icon {
        background-color: var(--main-color);
        border-bottom-color: var(--main-color);
        border-bottom-style: solid;
        border-bottom-width: 3px;
        border-left-color: var(--main-color);
        border-left-style: solid;
        border-left-width: 3px;
        border-right-color: var(--main-color);
        border-right-style: solid;
        border-right-width: 3px;
        border-top-color: var(--main-color);
        border-top-style: solid;
        border-top-width: 3px;
        box-sizing: content-box;
        color: rgb(255, 255, 255);
        font-size: 30px;
        height: 90px;
        line-height: 90px;
        margin-bottom: 0px;
        margin-left: 144.5px;
        margin-right: 144.5px;
        margin-top: 0px;
        padding-bottom: 0px;
        padding-left: 0px;
        padding-right: 0px;
        padding-top: 0px;
        position: relative;
        text-align: center;
        width: 90px;
        z-index: 9;
    }
    ul {
        padding: 0 !important;
    }
    @include md {
        .process .icon_list_icon {
            margin-left: 10px;
            margin-right: 10px;
        }
    }
    .icon_list_item h3 {
        margin: 15px;
        color: var(--main-color);
        font-size: 26px;
        font-weight: 700;
        line-height: 26px;
        text-align: center;
    }
    .icon_list_item .icon_list_connector {
        border: 1px dashed var(--main-color);
        position: absolute;
        text-transform: none;
        top: 45px;
        width: 385px;
        left: 192.5px
    }
    .process .text {
        width: 385px;
    }
    .process .text h3 {
        color: rgb(255, 255, 255);
        font-size: 26px;
        font-weight: 700;
        line-height: 36px;
        margin-bottom: 16px
    } 
    .process .text p {
        color: rgb(255, 255, 255);
        font-size: 16px;
        font-weight: 400;
        line-height: 28px;
    }
</style>