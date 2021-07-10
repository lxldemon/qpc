<template>
    <div id="HomeExpertsComponent">
        <div class="title">专家推荐</div>
        <div class="content">
            <div class="swiper-container">
                <div class="swiper-wrapper">
                    <div class="swiper-slide">Slide 1</div>
                    <div class="swiper-slide">Slide 2</div>
                    <div class="swiper-slide">Slide 3</div>
                </div>
                <!-- 如果需要分页器 -->
                <div class="swiper-pagination"></div>

                <!-- 如果需要导航按钮 -->
                <div class="swiper-button-prev"></div>
                <div class="swiper-button-next"></div>

                <!-- 如果需要滚动条 -->
                <div class="swiper-scrollbar"></div>
            </div>
        </div>
    </div>
</template>

<script>
    import Swiper from 'swiper';   // Import Swiper styles
    import 'swiper/dist/css/swiper.min.css';
    export default {
        components: {
            Swiper,
        },
        name: "HomeExpertsComponent",
        mounted(){
            new Swiper ('.swiper-container', {
                loop: true,
                speed: 400,
                spaceBetween: 100,
                // 如果需要分页器
                pagination: '.swiper-pagination',
                // 如果需要前进后退按钮
                nextButton: '.swiper-button-next',
                prevButton: '.swiper-button-prev',
                // 如果需要滚动条
                scrollbar: '.swiper-scrollbar',
            })
        },
        methods: {
            onSwiper(swiper) {
                console.log(swiper);
            },
            onSlideChange() {
                console.log('slide change');
            },
        },

    }
</script>

<style scoped >
    #HomeExpertsComponent{
        margin: 0 auto;
        margin-top: 31px;
        width: 80%;
        font-size: 18px;
    }
    #HomeExpertsComponent>.title{
        float: left;
    }
    #HomeExpertsComponent>.content{
        float: left;
        clear: both;
         width: 100%;
         height: 300px;
        margin: 20px auto;
    }
    .swiper-container{
        height: 200px;
        padding-left: 56px;
        background-image: -webkit-radial-gradient(23% 100%, #2e79c3 0%, #297bc4 100%);
    }

    .swiper-container .swiper-slide .active {
        color: #666;
        background-color: #fff8eb;
        box-shadow: 0 3px 13px 0 rgba(94, 94, 94, 0.50);
    }

</style>