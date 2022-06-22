<template>
  <section class="testimonials">
    <swiper
      :navigation="true"
      :modules="modules"
      class="mySwiper testimonials__swiper"
      :loop="true"
    >
      <swiper-slide class="testimonials__swiper__slide">
        <p class="testimonials__title">TESTIMONIALS</p>
        <p class="testimonials__text">
          Lorem ipsum dolor sit amet, consectetur adipiscing elit aliquam
        </p>
        <p class="testimonials__content">
          Lorem ipsum dolor sit amet, consectetuer adipiscing elit, sed diam
          nonummy nibh euismod tincidunt ut laoreet dolore magna aliquam erat
          volutpat. Ut wisi enim ad ortis nisl ut aliquio consequat.
        </p>
        <p class="testimonials__author"><span>Morton Reder</span>Co-Founder</p>
      </swiper-slide>
      <swiper-slide class="testimonials__swiper__slide">
        <p class="testimonials__title">TESTIMONIALS</p>
        <p class="testimonials__text">
          Lorem ipsum dolor sit amet, consectetur adipiscing elit aliquam
        </p>
        <p class="testimonials__content">
          Lorem ipsum dolor sit amet, consectetuer adipiscing elit, sed diam
          nonummy nibh euismod tincidunt ut laoreet dolore magna aliquam erat
          volutpat. Ut wisi enim ad ortis nisl ut aliquio consequat.
        </p>
        <p class="testimonials__author"><span>Morton Reder</span>Co-Founder</p>
      </swiper-slide>
    </swiper>
  </section>
</template>
<script>
import { Swiper, SwiperSlide } from "swiper/vue";
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
@import "../assets/styles/testimonials.scss";
</style>
