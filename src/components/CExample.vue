<template>
    <div class="container">
        <div id="content">
            <div id="slider">
                <div id="slider-content">
                    <swiper
                    :spaceBetween="30"
                    :effect="'fade'"
                    :navigation="false"
                    :pagination="false"
                    :modules="modules"
                    class="mySwiper"
                    ref="swiper"
                    >
                    <swiper-slide v-for="r in rs">
                        <div class="review">
    <div class="views-field views-field-field-project-logo">
        <div class="field-content">  
            <img loading="lazy" :src="require('@/'+r.image)" class="img-responsive">
        </div>
    </div>
    <div class="views-field views-field-field-report-text review-text">
        <div class="field-content">
            {{ r.text }}
        </div>
    </div>
    <div class="views-field review-author">
        <div class="field-content">{{ r.author }}</div>
    </div>
  </div>
</swiper-slide>
                    </swiper>
                </div>
                <nav>
                    <div class="m-auto">
                    <button type="button" class="slick-slide-prev slick-slide-arrow" ></button>
                                <span class="slide-num"><span class="slide-num-current">01</span> / 08</span>
                    <button type="button" class="slick-slide-next slick-slide-arrow"></button>
                    </div>
                </nav>
            </div>
    </div>
    </div>
  </template>
  <script>
  // Import Swiper Vue.js components
  import { Swiper, SwiperSlide } from "swiper/vue";
  
  // Import Swiper styles
  import "swiper/css";
  
  import "swiper/css/effect-fade";
  import "swiper/css/navigation";
  import "swiper/css/pagination";
  
  // import required modules
  import { EffectFade, Navigation, Pagination } from "swiper";
  import rs from '../data/reviews.json';
  export default {
    components: {
      Swiper,
      SwiperSlide,
    },
    setup() {
      return {
        modules: [EffectFade, Navigation, Pagination],
        rs
      };
    },
  };
  </script>

<style scoped>
img{
    height: 100%;
    widows: 100%;
    max-width: fit-content;
}
.review-text{
    margin-bottom: 28px;
    font-weight: bold;
    font-size: 14px;
    line-height: 1.2;
    color: #050c33;
    outline: 0;
}
.review-author{
    font-weight: 500;
    font-size: 14px;
    line-height: 1.2;
    color: #838b9c;
}
/* .review{
    width: 436px; 
    position: relative; 
    left: 0px; 
    top: 0px; 
    z-index: 998; 
    opacity: 0; 
    transition: opacity 500ms ease 0s;
} */
.slide-num{
    display: inline-block;
    margin: 0 46px;
    font-size: 28px;
    vertical-align: bottom;
    color: #e0e0e0;
}
.slick-slide-next{
    background: url(../assets/themes/arrow-right.svg) no-repeat center;
    background-size: contain;
}
.slick-slide-prev{
    background: url(../assets/themes/arrow-left.svg) no-repeat center;
    background-size: contain;
}

.slick-slide-arrow {
    width: 16px;
    height: 32px;
    border: 0;
    box-shadow: none;
    font-size: 0;
    outline: 0;
}
.slide-num-current{
    color: #050c33;
}
nav{
    width: 36%;
    float: left;
    display: flex;
}
#content{
    width: 980px;
    max-width: 100%;
    margin: auto;
    margin-top: 74px;
    position: relative;
}
#slider-content{
    width: 64%;
    float: left;
    padding-right: 60px;
    border-right: 1px solid #cdcdcd;
    padding: 14px 60px;
}
#slider{
    display: flex;
    flex-wrap: wrap;
    position: relative;
    z-index: 10;
    background: #fff;
    border: 1px solid rgba(0,0,0,.1);
    box-sizing: border-box;
    box-shadow: 0 4px 60px rgb(162 162 162 / 25%);
    border-radius: 5px;
    padding: 66px 0 66px 68px;
}

#slider::before{
    content: "";
    display: block;
    background: #fff;
    opacity: .5;
    border: 1px solid rgba(0,0,0,.1);
    box-sizing: border-box;
    box-shadow: 0 4px 60px rgb(162 162 162 / 25%);
    border-radius: 5px;
    position: absolute;
    top: -40px;
    bottom: 0;
    left: 64px;
    right: 64px;
    z-index: -1;
}

#slider::after{
    content: "";
    display: block;
    background: #fff;
    opacity: .34;
    border: 1px solid rgba(0,0,0,.1);
    box-sizing: border-box;
    box-shadow: 0 4px 60px rgb(162 162 162 / 25%);
    border-radius: 5px;
    position: absolute;
    top: -72px;
    bottom: 0;
    left: 128px;
    right: 128px;
    z-index: -2;
}
.swiper {
  width: 100%;
  height: 100%;
}

.swiper-slide {
  background-position: center;
  background-size: cover;
}

.swiper-slide img {
  display: block;
  width: 100%;
}
</style>