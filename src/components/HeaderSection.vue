<template>
  <section class="header">
    <swiper
      :navigation="true"
      :modules="modules"
      class="mySwiper header--swiper"
      :loop="true"
    >
      <swiper-slide class="header--swiper__slide">
        <img src="../assets/images/road-img.jpeg" />
        <div class="header--swiper__card">
          <p class="header--swiper__card__head">
            THEME FOR CREATIVES &DOING THEME BUSINESS NOW
          </p>
          <p class="header--swiper__card__text">for Themeforest</p>
          <div class="header--swiper__card__buttons">
            <button>Live Demo</button>
            <button>View Work</button>
          </div>
        </div>
      </swiper-slide>
      <swiper-slide class="header--swiper__slide">
        <img src="../assets/images/creative-img.jpeg" />
        <div class="header--swiper__card">
          <p class="header--swiper__card__head">
            THEME FOR CREATIVES &DOING THEME BUSINESS NOW
          </p>
          <p class="header--swiper__card__text">for Themeforest</p>
          <div class="header--swiper__card__buttons">
            <button>Live Demo</button>
            <button>View Work</button>
          </div>
        </div>
      </swiper-slide>
      <swiper-slide class="header--swiper__slide">
        <img src="../assets/images/digital-img.jpeg" />
        <div class="header--swiper__card">
          <p class="header--swiper__card__head">
            THEME FOR CREATIVES &DOING THEME BUSINESS NOW
          </p>
          <p class="header--swiper__card__text">for Themeforest</p>
          <div class="header--swiper__card__buttons">
            <button>Live Demo</button>
            <button>View Work</button>
          </div>
        </div>
      </swiper-slide>
    </swiper>
  </section>
</template>
<script>
import { Swiper, SwiperSlide } from "swiper/vue";
import "swiper/css";
import "swiper/css/navigation";
import { Navigation } from "swiper";

export default {
  components: {
    Swiper,
    SwiperSlide,
  },
  setup() {
    return {
      modules: [Navigation],
    };
  },
};
</script>

<style lang="scss">
@import "../assets/styles/header.scss";
</style>
