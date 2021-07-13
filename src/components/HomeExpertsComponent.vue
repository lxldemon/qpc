<template>
  <div id="HomeExpertsComponent">
    <div class="title">专家推荐</div>
    <div
      class="content"
      @mouseenter="onMouseMoveEnter"
      @mouseleave="onMouseMoveLeave"
    >
      <swiper class="swiper" :options="swiperOption" ref="mySwiper">
        <swiper-slide>Slide 1</swiper-slide>
        <swiper-slide>Slide 2</swiper-slide>
        <swiper-slide>Slide 3</swiper-slide>
        <swiper-slide>Slide 4</swiper-slide>
        <swiper-slide>Slide 5</swiper-slide>
        <swiper-slide>Slide 6</swiper-slide>
        <swiper-slide>Slide 7</swiper-slide>
        <swiper-slide>Slide 8</swiper-slide>
        <swiper-slide>Slide 9</swiper-slide>
        <swiper-slide>Slide 10</swiper-slide>

        <div class="swiper-pagination" slot="pagination"></div>
        <!-- 如果需要导航按钮 -->
        <div class="swiper-button-prev" slot="button-prev"></div>
        <div class="swiper-button-next" slot="button-next"></div>
      </swiper>
    </div>
  </div>
</template>

<script>
import { Swiper, SwiperSlide } from "vue-awesome-swiper";
import "swiper/swiper-bundle.min.css";
export default {
  components: {
    Swiper,
    SwiperSlide,
  },
  name: "HomeExpertsComponent",
  data() {
    return {
      swiperOption: {
        // 自动播放
        autoplay: {
          delay: 2000,
          disableOnInteraction: false,
        },
        // 每一次的间隔
        speed: 500,
        // 循环
        loop: true,
        // 窗口显示几个
        slidesPerView: 4,
        // 每一个的边距
        spaceBetween: 30,
        pagination: {
          el: ".swiper-pagination",
          clickable: true,
        },
        navigation: {
          nextEl: ".swiper-button-next",
          prevEl: ".swiper-button-prev",
        },
      },
    };
  },
  methods: {
    //通过获得的swiper对象来暂停自动播放
    /**
     * 鼠标引入暂停播放
     */
    onMouseMoveEnter() {
      this.$refs.mySwiper.swiperInstance.autoplay.stop();
    },
    /**
     * 鼠标离开继续
     */
    onMouseMoveLeave() {
      this.$refs.mySwiper.swiperInstance.autoplay.start();
    },
  },
  mounted() {},
};
</script>

<style scoped >
#HomeExpertsComponent {
  margin: 0 auto;
  margin-top: 31px;
  width: 80%;
  font-size: 18px;
}
#HomeExpertsComponent > .title {
  float: left;
}
#HomeExpertsComponent > .content {
  float: left;
  clear: both;
  width: 100%;
  height: 300px;
  margin: 20px auto;
}
.swiper-container {
  height: 200px;
  /* padding-left: 56px;
  padding-right: 56px; */
  /* background-image: -webkit-radial-gradient(23% 100%, #2e79c3 0%, #297bc4 100%); */
}

/* .swiper-container .swiper-slide .active {
  color: #666;
  background-color: #fff8eb;
  box-shadow: 0 3px 13px 0 rgba(94, 94, 94, 0.5);
} */

.swiper-slide {
  text-align: center;
  font-size: 18px;
  background: #fff;
  display: flex;
  justify-content: center;
  align-items: center;
}

.swiper-slide img {
  display: block;
  width: 100%;
  height: 100%;
  object-fit: cover;
}
</style>